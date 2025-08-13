---
difficulty: intermediate
prerequisites: ["basic-css", "css-box-model"]
learning_objectives: ["Use flexbox for layouts", "Control flex item alignment", "Create responsive designs"]
tags: ["css", "layout", "flexbox"]
last_reviewed: 2025-08-13
confidence: 1
connections: ["basic-css", "centering-a-div", "css-grid", "responsive-centering"]
---

# Flexbox Basics

## Core Concept
Flexbox is a CSS layout method that arranges items in a flexible container. It makes it easy to align, distribute, and resize elements within a container.

## Why It Matters
Flexbox solves many common layout problems like centering, equal-height columns, and responsive design with minimal code. It's essential for modern web layouts.

## Step-by-Step

### 1. Create a Flex Container
```css
.container {
  display: flex;
}
```

### 2. Control Direction
```css
.row { flex-direction: row; }        /* default: left to right */
.column { flex-direction: column; }  /* top to bottom */
```

### 3. Align Items
```css
.container {
  display: flex;
  justify-content: center;    /* horizontal alignment */
  align-items: center;        /* vertical alignment */
}
```

### 4. Common Alignment Values
```css
/* justify-content (horizontal) */
flex-start | flex-end | center | space-between | space-around

/* align-items (vertical) */
flex-start | flex-end | center | stretch | baseline
```

## Common Mistakes
- Forgetting `display: flex` on the container
- Confusing `justify-content` and `align-items`
- Not understanding that flex properties apply to the parent container

## Practice
Create a navigation bar with centered items:
```html
<nav class="navbar">
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Contact</a>
</nav>
```

## Next Steps
- [[centering-a-div]] - Apply flexbox to centering
- [[css-grid]] - Learn alternative layout system
- [[responsive-centering]] - Make layouts adapt to screen size