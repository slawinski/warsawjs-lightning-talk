# CSS Centering Examples

🎯 **Practical examples** of different centering techniques in action. These hands-on examples demonstrate the concepts from [[Centering Divs]], [[CSS Flexbox]], [[CSS Grid]], and other centering methods.

## Brief Explanation

🔧 Learning centering is best done through practice. These examples progress from simple to complex, showing real-world scenarios where different centering techniques excel.

## Prerequisites

- [[CSS Basics]] - Understanding properties and selectors
- [[HTML Basics]] - Basic markup structure
- [[CSS Box Model]] - How elements occupy space
- [[CSS Flexbox]] - Modern layout fundamentals

## Basic Centering Examples

### 🌟 Example 1: Simple Horizontal Center
```html
<div class="container">
  <div class="box">Centered Box</div>
</div>
```

```css
.container {
  width: 100%;
  background: #f0f0f0;
  padding: 20px;
}

.box {
  width: 200px;
  height: 100px;
  background: #007bff;
  color: white;
  text-align: center;
  line-height: 100px;
  margin: 0 auto;        /* [[CSS Margin Auto]] */
}
```

### 🌟 Example 2: Perfect Center with Flexbox
```html
<div class="flex-container">
  <div class="centered-content">
    <h2>Perfectly Centered</h2>
    <p>Both horizontally and vertically!</p>
  </div>
</div>
```

```css
.flex-container {
  display: flex;
  justify-content: center;  /* horizontal center */
  align-items: center;      /* vertical center */
  height: 100vh;           /* full viewport height */
  background: #f8f9fa;
}

.centered-content {
  background: white;
  padding: 40px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  text-align: center;
}
```

### 🌟 Example 3: Grid Perfect Center
```html
<div class="grid-container">
  <div class="grid-item">Grid Centered</div>
</div>
```

```css
.grid-container {
  display: grid;
  place-items: center;     /* centers both ways */
  height: 100vh;
  background: #e9ecef;
}

.grid-item {
  background: #28a745;
  color: white;
  padding: 30px 50px;
  border-radius: 5px;
}
```

## Real-World Scenarios

### 🎨 Example 4: Modal Dialog
```html
<div class="modal-overlay">
  <div class="modal">
    <h3>Confirmation</h3>
    <p>Are you sure you want to delete this item?</p>
    <div class="modal-buttons">
      <button class="cancel">Cancel</button>
      <button class="confirm">Delete</button>
    </div>
  </div>
</div>
```

```css
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0,0,0,0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  background: white;
  padding: 30px;
  border-radius: 8px;
  width: 90%;
  max-width: 400px;
  text-align: center;
}

.modal-buttons {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 20px;
}
```

### 🎨 Example 5: Card Layout
```html
<div class="cards-container">
  <div class="card">Card 1</div>
  <div class="card">Card 2</div>
  <div class="card">Card 3</div>
</div>
```

```css
.cards-container {
  display: flex;
  justify-content: center;   /* center the group */
  align-items: center;       /* center vertically */
  gap: 20px;                /* space between cards */
  min-height: 50vh;
  flex-wrap: wrap;          /* wrap on small screens */
}

.card {
  width: 200px;
  height: 150px;
  background: #6c757d;
  color: white;
  display: flex;
  justify-content: center;   /* center card content */
  align-items: center;
  border-radius: 8px;
}
```

### 🎨 Example 6: Form Centering
```html
<div class="form-wrapper">
  <form class="login-form">
    <h2>Login</h2>
    <input type="email" placeholder="Email">
    <input type="password" placeholder="Password">
    <button type="submit">Sign In</button>
  </form>
</div>
```

```css
.form-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: #f8f9fa;
  padding: 20px;
}

.login-form {
  background: white;
  padding: 40px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  width: 100%;
  max-width: 400px;
}

.login-form h2 {
  text-align: center;
  margin-bottom: 30px;
}

.login-form input,
.login-form button {
  width: 100%;
  padding: 12px;
  margin-bottom: 15px;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-sizing: border-box;
}

.login-form button {
  background: #007bff;
  color: white;
  border: none;
  cursor: pointer;
}
```

## Advanced Examples

### 🚀 Example 7: Hero Section
```html
<section class="hero">
  <div class="hero-content">
    <h1>Welcome to Our Site</h1>
    <p>Creating amazing web experiences</p>
    <button class="cta-button">Get Started</button>
  </div>
</section>
```

```css
.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
}

.hero-content h1 {
  font-size: 3rem;
  margin-bottom: 20px;
}

.hero-content p {
  font-size: 1.2rem;
  margin-bottom: 30px;
}

.cta-button {
  background: white;
  color: #667eea;
  padding: 15px 30px;
  border: none;
  border-radius: 25px;
  font-size: 1.1rem;
  cursor: pointer;
}
```

### 🚀 Example 8: Complex Grid Layout
```html
<div class="dashboard">
  <div class="widget">Widget 1</div>
  <div class="widget main-widget">Main Content</div>
  <div class="widget">Widget 3</div>
</div>
```

```css
.dashboard {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: 1fr auto 1fr;
  height: 100vh;
  gap: 20px;
  padding: 20px;
}

.widget {
  background: #343a40;
  color: white;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.2rem;
}

.main-widget {
  grid-column: 2;
  grid-row: 2;
  background: #007bff;
}
```

## Related Concepts

- [[CSS Flexbox]] - Modern flexible layouts
- [[CSS Grid]] - Two-dimensional layout system
- [[CSS Margin Auto]] - Traditional horizontal centering
- [[Responsive Design]] - Making layouts work on all devices
- [[CSS Position Absolute]] - Alternative positioning methods

## Next Steps

1. Practice modifying these examples with different content
2. Learn [[Responsive Design]] - making centers work on all devices
3. Explore [[Advanced CSS Layouts]] - combining multiple techniques
4. Study [[CSS Layout Methods]] - comprehensive layout overview

## Exercise Ideas

🎯 **Try these modifications:**
- Change the flexbox direction and see how centering adapts
- Add responsive breakpoints to the examples
- Combine grid and flexbox in the same layout
- Create a photo gallery with centered thumbnails
- Build a pricing table with centered cards

💡 **Pro Tip**: Start with simple examples and gradually add complexity - each technique builds on the previous ones!