# CSS Flexbox

🌟 **CSS Flexbox** (Flexible Box Layout) is a powerful one-dimensional layout method that makes it easy to distribute space and align items in a container, even when their size is unknown or dynamic.

## Brief Explanation

🔧 Flexbox provides a more efficient way to lay out, distribute, and align items in a container. It's particularly excellent for [[Centering Divs]] and creating responsive layouts without complex calculations.

## Prerequisites

- [[CSS Basics]] - Understanding selectors, properties, and values
- [[HTML Basics]] - Knowledge of HTML structure and elements
- [[CSS Box Model]] - How elements occupy space

## Core Concepts

### 🎯 Main Axis vs Cross Axis
- **Main Axis**: The primary axis along which flex items are laid out
- **Cross Axis**: The axis perpendicular to the main axis
- Direction controlled by `flex-direction`

### 🔄 Flex Container Properties
```css
.container {
  display: flex; /* or inline-flex */
  flex-direction: row | column | row-reverse | column-reverse;
  justify-content: flex-start | center | flex-end | space-between | space-around | space-evenly;
  align-items: stretch | flex-start | center | flex-end | baseline;
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

### 🎨 Flex Item Properties
```css
.item {
  flex-grow: 0; /* ability to grow */
  flex-shrink: 1; /* ability to shrink */
  flex-basis: auto; /* initial main size */
  align-self: auto | flex-start | center | flex-end | stretch;
}
```

## Common Centering Patterns

### Perfect Center
```css
.center-everything {
  display: flex;
  justify-content: center; /* horizontal center */
  align-items: center;     /* vertical center */
  height: 100vh;          /* full viewport height */
}
```

### Horizontal Center Only
```css
.center-horizontal {
  display: flex;
  justify-content: center;
}
```

### Vertical Center Only
```css
.center-vertical {
  display: flex;
  align-items: center;
  height: 200px; /* container needs height */
}
```

## Related Concepts

- [[CSS Grid]] - Two-dimensional layout alternative
- [[CSS Position Absolute]] - Traditional positioning method
- [[CSS Margin Auto]] - Simple horizontal centering
- [[Responsive Design]] - Making flexible layouts
- [[CSS Layout Methods]] - Overview of all layout techniques

## Next Steps

1. Practice with [[CSS Centering Examples]] - hands-on flexbox exercises
2. Learn [[CSS Grid]] for two-dimensional layouts
3. Explore [[Advanced Flexbox Patterns]] for complex scenarios
4. Study [[CSS Layout Methods]] for comprehensive understanding

## Browser Support

✅ **Excellent**: Supported in all modern browsers
⚠️ **Note**: IE11 has some flexbox bugs but basic centering works

💡 **Pro Tip**: Start with flexbox for most layout needs - it's intuitive and powerful!