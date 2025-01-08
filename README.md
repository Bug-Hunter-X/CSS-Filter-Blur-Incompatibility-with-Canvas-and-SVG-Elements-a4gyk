# CSS Filter Blur Incompatibility

This repository demonstrates a common issue with the CSS `filter: blur()` property: its incompatibility with certain HTML5 elements such as `<canvas>` and `<svg>`.  The problem is that `filter` operates on the rendering context of the element, and elements without a filter-compatible rendering context will not render the blur effect.

## Steps to Reproduce
1. Clone the repository.
2. Open `bug.html` in your browser.
3. Observe that the blur filter is applied to the `<div>` but not to the `<canvas>` or `<svg>`. 

## Solution
The solution involves applying the blur using a different approach, such as applying the blur to a wrapper element that surrounds the problematic element or using JavaScript to manipulate the canvas or SVG rendering context directly.