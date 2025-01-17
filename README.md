# Uncommon HTML Error: Non-Existent Property vs. Attribute Access

This repository demonstrates an uncommon error in HTML related to accessing non-existent properties versus attributes on DOM elements.  The core difference lies in how the browser handles these two scenarios.

## Bug Description

The bug highlights the unexpected behavior when attempting to access a non-existent attribute using `getAttribute()` compared to directly accessing a non-existent property on a DOM element.  `getAttribute()` gracefully handles the absence of the attribute by returning `null`, while accessing a non-existent property results in a runtime error in strict mode.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Observe the console output.  You'll see that accessing a non-existent attribute returns `null`, while accessing a non-existent property throws an error.

## Solution

The solution involves careful consideration of how you access properties and attributes.  Always check for the existence of properties before accessing them to avoid runtime errors or use try...catch blocks for error handling.

The `bugSolution.html` shows safe practices to avoid this error. Note that it is always recommended to check for null before any property access to prevent runtime errors.