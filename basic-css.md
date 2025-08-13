---
difficulty: beginner
prerequisites: ["html-elements"]
learning_objectives: ["Write basic CSS syntax", "Apply styles to HTML elements", "Use selectors effectively"]
tags: ["css", "fundamentals", "styling"]
last_reviewed: 2025-08-13
confidence: 1
connections: ["html-elements", "css-box-model", "centering-a-div"]
---

# Basic CSS

## Core Concept
CSS (Cascading Style Sheets) controls how HTML elements look on the page. It uses selectors to target elements and properties to define their appearance.

## Why It Matters
CSS transforms plain HTML into visually appealing web pages. Without CSS, websites would be just black text on white backgrounds.

## Step-by-Step

### 1. Basic Syntax
```css
selector {
  property: value;
}
```

### 2. Common Selectors
```css
/* Element selector */
p { color: blue; }

/* Class selector */
.my-class { font-size: 18px; }

/* ID selector */
#my-id { background: yellow; }
```

### 3. Essential Properties
```css
.example {
  color: red;           /* text color */
  background: white;    /* background color */
  width: 200px;        /* element width */
  height: 100px;       /* element height */
  margin: 10px;        /* space outside */
  padding: 5px;        /* space inside */
}
```

## Common Mistakes
- Forgetting semicolons after property values
- Mixing up class (.) and ID (#) selectors
- Not understanding CSS specificity rules

## Practice
Style a paragraph to be red, centered, and have a blue background:
```html
<p class="styled-text">Hello World</p>
```

## Next Steps
- [[css-box-model]] - Understand spacing and sizing
- [[centering-a-div]] - Learn layout positioning