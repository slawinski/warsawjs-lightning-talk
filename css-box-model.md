---
difficulty: beginner
prerequisites: ["basic-css", "html-elements"]
learning_objectives: ["Understand content, padding, border, margin", "Control element spacing", "Debug layout issues"]
tags: ["css", "fundamentals", "spacing"]
last_reviewed: 2025-08-13
confidence: 1
connections: ["basic-css", "centering-a-div", "flexbox-basics", "css-grid"]
---

# CSS Box Model

## Core Concept
Every HTML element is a rectangular box with four areas: content, padding, border, and margin. Understanding this model is crucial for controlling spacing and layout.

## Why It Matters
The box model determines how elements take up space and interact with each other. Mastering it prevents layout surprises and helps you create precise designs.

## Step-by-Step

### 1. The Four Areas (Inside to Outside)
```
┌─── margin ────────────┐
│ ┌─── border ────────┐ │
│ │ ┌─── padding ──┐ │ │
│ │ │   content    │ │ │
│ │ └──────────────┘ │ │
│ └──────────────────┘ │
└──────────────────────┘
```

### 2. CSS Properties
```css
.box {
  content: 200px;        /* width and height */
  padding: 20px;         /* space inside border */
  border: 5px solid red; /* border around content+padding */
  margin: 10px;          /* space outside border */
}
```

### 3. Shorthand Properties
```css
.example {
  /* All sides */
  margin: 20px;
  
  /* Vertical | Horizontal */
  padding: 10px 20px;
  
  /* Top | Right | Bottom | Left */
  margin: 10px 15px 20px 25px;
}
```

### 4. Box-Sizing Property
```css
.border-box {
  box-sizing: border-box;  /* width includes padding and border */
}

.content-box {
  box-sizing: content-box; /* default: width is just content */
}
```

## Common Mistakes
- Not understanding how `box-sizing` affects width calculations
- Forgetting that margins can collapse between adjacent elements
- Using padding when margin is needed (or vice versa)

## Practice
Create a 200px box that stays 200px even with padding and border:
```css
.fixed-box {
  width: 200px;
  padding: 20px;
  border: 5px solid blue;
  box-sizing: border-box;
}
```

## Next Steps
- [[centering-a-div]] - Apply box model to centering techniques
- [[flexbox-basics]] - Use flexbox with proper spacing
- [[css-grid]] - Combine grid with box model understanding