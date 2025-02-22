# CSS calc() Miscalculation Bug

This repository demonstrates a common error when using the `calc()` function in CSS to calculate widths involving both percentages and pixels.  The issue arises from the order of operations and can lead to unexpected results or invalid negative widths.

## Bug Description

The provided CSS uses `calc()` to subtract a fixed pixel value from a percentage-based width. While seemingly straightforward, the calculation's outcome depends on the parent container's width, potentially resulting in negative values if the parent is too narrow.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the problematic CSS.
3. Open `index.html` (or any HTML file with a similarly styled element) to observe the unexpected width behavior.  Try changing the parent container's width to see the varying results.

## Solution

The solution, demonstrated in `bugSolution.css`, involves restructuring the `calc()` expression to ensure proper order of operations or using alternative calculation methods to avoid the problem.