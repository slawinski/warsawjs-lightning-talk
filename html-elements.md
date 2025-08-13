---
difficulty: beginner
prerequisites: []
learning_objectives: ["Create basic HTML structure", "Use common HTML tags", "Understand semantic markup"]
tags: ["html", "fundamentals", "markup"]
last_reviewed: 2025-08-13
confidence: 1
connections: ["basic-css", "centering-a-div"]
---

# HTML Elements

## Core Concept
HTML elements are the building blocks of web pages. They define structure and content using tags wrapped in angle brackets.

## Why It Matters
HTML provides the foundation for all web content. Understanding elements is essential before you can style them with CSS or make them interactive with JavaScript.

## Step-by-Step

### 1. Basic Structure
```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
</head>
<body>
  <h1>Main Heading</h1>
  <p>A paragraph of text.</p>
</body>
</html>
```

### 2. Common Elements
```html
<div>Generic container</div>
<span>Inline container</span>
<p>Paragraph text</p>
<h1>Large heading</h1>
<h2>Smaller heading</h2>
<a href="link.html">Link</a>
<img src="image.jpg" alt="Description">
```

### 3. Block vs Inline
- **Block elements**: Take full width (div, p, h1)
- **Inline elements**: Only take needed space (span, a, img)

## Common Mistakes
- Forgetting closing tags
- Mixing up block and inline behavior
- Not using semantic elements appropriately

## Practice
Create a simple page with a heading, paragraph, and div container:
```html
<div class="container">
  <h1>Welcome</h1>
  <p>This is my first webpage.</p>
</div>
```

## Next Steps
- [[basic-css]] - Style your HTML elements
- [[centering-a-div]] - Learn layout positioning