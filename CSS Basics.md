# CSS Basics

🎨 **CSS (Cascading Style Sheets)** is the language used to describe the presentation and styling of HTML documents. It controls how web pages look and feel.

## Brief Explanation

🔧 CSS separates content (HTML) from presentation, allowing you to control layout, colors, fonts, spacing, and visual effects. It's essential for [[Centering Divs]] and all web styling.

## Prerequisites

- [[HTML Basics]] - Understanding document structure and elements
- Basic understanding of web browsers and how they work

## Core Concepts

### 🎯 CSS Syntax
```css
selector {
  property: value;
  property: value;
}
```

### 🌟 Common Selectors
```css
/* Element selector */
p { color: blue; }

/* Class selector */
.my-class { font-size: 16px; }

/* ID selector */
#my-id { background: red; }

/* Descendant selector */
div p { margin: 10px; }
```

### 🔄 Essential Properties for Layout
```css
.element {
  /* Display types */
  display: block | inline | inline-block | flex | grid;
  
  /* Box model */
  width: 300px;
  height: 200px;
  padding: 20px;
  margin: 10px;
  border: 1px solid black;
  
  /* Positioning */
  position: static | relative | absolute | fixed | sticky;
  top: 0;
  left: 0;
}
```

## Key Layout Properties

### 🎨 Display Property
- `block`: Full width, stacks vertically
- `inline`: Only as wide as content, flows horizontally
- `inline-block`: Hybrid of block and inline
- `flex`: Enables [[CSS Flexbox]] layout
- `grid`: Enables [[CSS Grid]] layout

### 📏 Box Model Components
- **Content**: The actual content area
- **Padding**: Space inside the element
- **Border**: Line around the element
- **Margin**: Space outside the element

## CSS for Centering Foundation

### 🎯 Text Alignment
```css
.text-center {
  text-align: center; /* Centers inline content */
}
```

### 🎯 Block Element Centering
```css
.center-block {
  margin: 0 auto; /* Horizontal center */
  width: 300px;   /* Width required */
}
```

## Related Concepts

- [[CSS Box Model]] - How elements take up space
- [[CSS Display Property]] - How elements behave in layout
- [[CSS Flexbox]] - Modern flexible layouts
- [[CSS Grid]] - Two-dimensional layout system
- [[CSS Position Absolute]] - Precise element positioning

## Next Steps

1. Master [[CSS Box Model]] - fundamental for all layout
2. Learn [[CSS Display Property]] - controls element behavior
3. Practice [[Centering Divs]] - applying CSS basics
4. Explore [[CSS Layout Methods]] - comprehensive overview

## How CSS Works

🌐 **Cascade**: Styles can come from multiple sources
🎯 **Specificity**: More specific selectors override less specific ones
💡 **Inheritance**: Some properties pass from parent to child

💡 **Pro Tip**: Master the box model first - it's the foundation of all CSS layout!