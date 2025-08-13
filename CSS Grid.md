# CSS Grid

🚀 **CSS Grid** is a two-dimensional layout system that provides precise control over both rows and columns simultaneously. It's perfect for complex layouts and offers elegant solutions for [[Centering Divs]].

## Brief Explanation

🔧 Grid Layout allows you to create sophisticated web layouts with clean, semantic markup. Unlike [[CSS Flexbox]] which is one-dimensional, Grid works with both dimensions at once.

## Prerequisites

- [[CSS Basics]] - Understanding selectors and properties
- [[HTML Basics]] - Document structure knowledge
- [[CSS Box Model]] - How elements interact with space
- [[CSS Flexbox]] - Understanding one-dimensional layouts first

## Core Concepts

### 🎯 Grid Container Properties
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* column sizes */
  grid-template-rows: 100px auto;     /* row sizes */
  gap: 20px;                          /* spacing between items */
  justify-items: start | center | end | stretch;
  align-items: start | center | end | stretch;
  place-items: center; /* shorthand for both */
}
```

### 🌐 Grid Item Properties
```css
.item {
  grid-column: 1 / 3;     /* span from line 1 to 3 */
  grid-row: 2;            /* place in row 2 */
  justify-self: center;   /* horizontal alignment */
  align-self: center;     /* vertical alignment */
  place-self: center;     /* shorthand for both */
}
```

## Centering Techniques

### 🎨 Perfect Center (Simplest)
```css
.center-container {
  display: grid;
  place-items: center;
  height: 100vh;
}
```

### 🎨 Center with Multiple Items
```css
.grid-center {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  grid-template-rows: 1fr auto 1fr;
}

.centered-item {
  grid-column: 2;
  grid-row: 2;
}
```

### 🎨 Center in Named Areas
```css
.layout {
  display: grid;
  grid-template-areas: 
    ". . ."
    ". center ."
    ". . .";
  grid-template-columns: 1fr auto 1fr;
  grid-template-rows: 1fr auto 1fr;
}

.center-item {
  grid-area: center;
}
```

## Grid vs Flexbox

🔄 **When to use Grid**:
- Two-dimensional layouts (rows AND columns)
- Complex, structured layouts
- When you need precise item placement

🔄 **When to use Flexbox**:
- One-dimensional layouts (row OR column)
- Simple centering tasks
- Dynamic content that should flow

## Related Concepts

- [[CSS Flexbox]] - One-dimensional layout companion
- [[CSS Subgrid]] - Advanced nested grid layouts
- [[CSS Grid Areas]] - Named template areas for cleaner code
- [[Responsive Design]] - Creating adaptive grid layouts
- [[CSS Layout Methods]] - Comprehensive layout overview

## Next Steps

1. Master [[CSS Grid Areas]] for semantic layouts
2. Practice with [[CSS Centering Examples]] - grid-focused exercises
3. Learn [[CSS Subgrid]] for advanced nested scenarios
4. Explore [[Advanced CSS Layouts]] combining Grid and Flexbox

## Browser Support

✅ **Excellent**: Supported in all modern browsers
⚠️ **IE11**: Partial support with older syntax

💡 **Pro Tip**: Use `place-items: center` for the quickest perfect centering with Grid!