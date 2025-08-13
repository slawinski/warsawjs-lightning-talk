# 🗄️ Cache API

## Overview
💾 **Cache API** provides a browser-based storage mechanism for HTTP requests and responses, enabling offline functionality and performance improvements. It's a key component for implementing [[Progressive Web Apps]] offline capabilities.

## Key Characteristics
- 🌐 **Request/Response Storage**: Stores network requests and their responses
- ⚡ **Persistent**: Data survives browser restarts
- 🔒 **Origin-Bound**: Each origin has its own cache storage
- 🎯 **Programmatic**: Full JavaScript control over caching
- 🔄 **Works with [[Service Workers]]**: Primary use case for offline functionality

## Prerequisites
- [[JavaScript Fundamentals]] - Promises, async/await
- [[HTTP Protocol]] - Understanding requests and responses
- [[Service Workers]] - Background scripts for offline functionality
- [[Fetch API]] - Modern network request interface

## Basic Operations

### Opening a Cache
```javascript
// Open or create a named cache
const cache = await caches.open('my-cache-v1');
```

### Adding Resources
```javascript
// Add single resource
await cache.add('/index.html');

// Add multiple resources
await cache.addAll([
  '/styles.css',
  '/script.js',
  '/images/logo.png'
]);
```

### Retrieving from Cache
```javascript
// Check if request is cached
const response = await cache.match('/index.html');
if (response) {
  // Use cached response
}
```

## Cache Strategies

### Cache First
🏠 Serve from cache, fallback to network
```javascript
const response = await cache.match(request) || fetch(request);
```

### Network First  
🌐 Try network first, fallback to cache
```javascript
try {
  const response = await fetch(request);
  cache.put(request, response.clone());
  return response;
} catch {
  return cache.match(request);
}
```

### Cache Only
⚡ Only serve from cache
```javascript
const response = await cache.match(request);
```

### Network Only
🔄 Only serve from network
```javascript
const response = await fetch(request);
```

### Stale While Revalidate
🎯 Serve cache, update in background
```javascript
const cachedResponse = cache.match(request);
const fetchPromise = fetch(request).then(response => {
  cache.put(request, response.clone());
  return response;
});
return cachedResponse || fetchPromise;
```

## Cache Management

### Listing Caches
```javascript
const cacheNames = await caches.keys();
```

### Deleting Caches
```javascript
// Delete specific cache
await caches.delete('old-cache-v1');

// Delete old versions
cacheNames.forEach(name => {
  if (name !== 'current-cache-v2') {
    caches.delete(name);
  }
});
```

### Cache Inspection
```javascript
// List cached requests
const requests = await cache.keys();

// Check cache contents
for (const request of requests) {
  const response = await cache.match(request);
  console.log(request.url, response.status);
}
```

## Advanced Patterns

### Runtime Caching
Cache resources as they're requested:
```javascript
self.addEventListener('fetch', event => {
  event.respondWith(
    cache.match(event.request).then(response => {
      if (response) return response;
      
      return fetch(event.request).then(response => {
        cache.put(event.request, response.clone());
        return response;
      });
    })
  );
});
```

### Selective Caching
Only cache specific types of requests:
```javascript
if (request.destination === 'image') {
  // Cache images
  cache.put(request, response.clone());
}
```

## Storage Considerations

### Storage Limits
- [[Browser Storage Quotas]] - Understanding storage limits
- [[Storage Management]] - Efficient usage patterns
- [[Cache Cleanup]] - Removing old or unused data

### Cache Versioning
- Use version numbers in cache names
- Clean up old versions during [[Service Worker]] activation
- Handle cache updates gracefully

## Performance Optimization

### Preloading Critical Resources
```javascript
// During service worker installation
const criticalResources = ['/app-shell.html', '/critical.css'];
await cache.addAll(criticalResources);
```

### Background Updates
Update cache without blocking user requests:
```javascript
// Update cache in background
fetch(request).then(response => {
  cache.put(request, response.clone());
});
```

## Tools and Libraries
- 🧰 [[Workbox]] - Google's caching library with advanced strategies
- 🔍 [[Chrome DevTools]] - Inspect cache contents and behavior
- 📊 [[Cache Inspector]] - Analyze cache usage and effectiveness
- 🛠️ [[PWA Builder]] - Generate caching strategies

## Best Practices
- Version your caches for easy updates
- Implement [[Cache Cleanup]] strategies
- Cache essential resources during installation
- Use appropriate caching strategies per resource type
- Monitor cache storage usage

## Common Pitfalls
- Forgetting to clone responses when caching
- Not handling cache update scenarios
- Caching too many or too large resources
- Missing error handling for cache operations

## Debugging Techniques
- [[Cache Debugging]] - Chrome DevTools techniques
- [[Offline Testing]] - Verify cache behavior
- [[Cache Performance]] - Monitor cache hit rates
- [[Storage Analysis]] - Track cache storage usage

## Related Concepts
- [[Service Workers]] - Background scripts using Cache API
- [[Offline-First Strategy]] - Design approach using caching
- [[Application Shell Architecture]] - Caching pattern for PWAs
- [[Browser Storage]] - Other storage options (localStorage, IndexedDB)
- [[HTTP Caching]] - Server-side caching headers

## Next Steps
- Implement basic caching with [[Cache API Tutorial]]
- Learn [[Advanced Caching Strategies]]
- Explore [[Workbox]] for production-ready solutions
- Study [[Cache Performance Optimization]]