---
difficulty: intermediate
prerequisites: ["basic-css", "css-box-model"]
learning_objectives: ["Create grid layouts", "Position items in grid areas", "Use grid for complex layouts"]
tags: ["css", "layout", "grid"]
last_reviewed: 2025-08-13
confidence: 1
connections: ["basic-css", "flexbox-basics", "centering-a-div", "responsive-centering"]
---

# CSS Grid

## Core Concept
CSS Grid is a two-dimensional layout system that lets you create complex layouts with rows and columns. Unlike flexbox (which is one-dimensional), grid handles both directions simultaneously.

## Why It Matters
Grid excels at creating complex, magazine-style layouts and is perfect for centering items with minimal code. It's the most powerful layout tool in modern CSS.

## Step-by-Step

### 1. Create a Grid Container
```css
.container {
  display: grid;
}
```

### 2. Define Grid Structure
```css
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;  /* 3 equal columns */
  grid-template-rows: 100px 200px;     /* 2 rows with set heights */
  gap: 20px;                           /* spacing between items */
}
```

### 3. Center Items (Easiest Method)
```css
.center-grid {
  display: grid;
  place-items: center;  /* centers both horizontally and vertically */
  height: 100vh;
}
```

### 4. Position Specific Items
```css
.item {
  grid-column: 2 / 4;  /* spans from column 2 to 4 */
  grid-row: 1 / 3;     /* spans from row 1 to 3 */
}
```

## Common Mistakes
- Confusing `place-items` (aligns content) with `place-content` (aligns the grid itself)
- Not understanding the difference between implicit and explicit grid lines
- Overcomplicating simple layouts that flexbox could handle better

## Practice
Create a 3×3 grid with a centered item:
```html
<div class="grid-container">
  <div class="grid-item">Centered</div>
</div>
```

## Next Steps
- [[centering-a-div]] - Compare grid vs flexbox centering
- [[flexbox-basics]] - Learn when to use flex vs grid
- [[responsive-centering]] - Make grids responsive