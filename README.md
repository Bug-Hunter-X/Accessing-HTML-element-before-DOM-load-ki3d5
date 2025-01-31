# Uncommon HTML Bug: Accessing Element Before DOM Load

This repository demonstrates a common yet easily missed error in HTML and JavaScript interaction: attempting to access and manipulate a DOM element before the browser has fully parsed and loaded it.  This often leads to a `null` reference error, as the element doesn't exist in the DOM yet when the JavaScript attempts to access it.

The `bug.html` file showcases the error, and `solution.html` provides the corrected version, utilizing an event listener to ensure the element is available.

## How to Reproduce the Bug

1. Open `bug.html` in a web browser.
2. Observe the JavaScript error in your browser's console.

## Solution

The solution is to leverage the `DOMContentLoaded` event, which fires when the initial HTML document has been completely loaded and parsed.  This guarantees that the element you're targeting will exist when your JavaScript attempts to access it.