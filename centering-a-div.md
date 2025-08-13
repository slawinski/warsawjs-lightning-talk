---
difficulty: beginner
prerequisites: ["basic-css", "html-elements"]
learning_objectives: ["Center divs horizontally", "Center divs vertically", "Choose appropriate centering method"]
tags: ["css", "layout", "positioning"]
last_reviewed: 2025-08-13
confidence: 1
connections: ["flexbox-basics", "css-grid", "css-box-model"]
---

# How to Center a Div

## Core Concept
Centering a div means positioning it in the middle of its container, either horizontally, vertically, or both. There are several CSS methods to achieve this.

## Why It Matters
Centering elements is one of the most common layout tasks in web development. Mastering these techniques will make your layouts look professional and properly aligned.

## Step-by-Step

### 1. Horizontal Centering (Classic Method)
```css
.horizontal-center {
  margin: 0 auto;
  width: 300px; /* Must have a defined width */
}
```

### 2. Vertical Centering with Flexbox
```css
.vertical-center {
  display: flex;
  align-items: center;
  height: 100vh; /* Container needs height */
}
```

### 3. Both Directions with Flexbox (Most Common)
```css
.center-both {
  display: flex;
  justify-content: center; /* horizontal */
  align-items: center;     /* vertical */
  height: 100vh;
}
```

### 4. Using CSS Grid (Modern Approach)
```css
.grid-center {
  display: grid;
  place-items: center;
  height: 100vh;
}
```

## Common Mistakes
- Forgetting to set a width for `margin: 0 auto`
- Not giving the container a height for vertical centering
- Using `text-align: center` on block elements (only works for inline content)
- Mixing old and new centering methods unnecessarily

## Practice
Try centering a 200px × 200px red div in the middle of your viewport:
```html
<div class="container">
  <div class="centered-box">I'm centered!</div>
</div>
```

## Next Steps
- [[flexbox-basics]] - Learn more about flexible layouts
- [[css-grid]] - Master grid-based centering
- [[responsive-centering]] - Make centering work on all devices