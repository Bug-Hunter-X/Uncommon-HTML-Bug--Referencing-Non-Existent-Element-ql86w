# Uncommon HTML Bug: Referencing a Non-Existent Element

This repository demonstrates a common yet easily missed error in HTML: attempting to manipulate a DOM element that doesn't exist using JavaScript.  The bug occurs when JavaScript code tries to access an element using `document.getElementById()` or a similar method, but that element is not present in the HTML structure.

## Bug Description

The `bug.html` file contains a simple HTML page that includes a script that attempts to add content to a div with the ID 'myDiv'. However, if the element is not found, it causes a runtime error.

## Solution

The `solution.html` file demonstrates how to solve the problem by ensuring the element is present before attempting to manipulate it. This can be done using a variety of techniques, such as:

1. **Checking for null:** Ensure that `document.getElementById('myDiv')` returns a valid element before attempting to modify its contents.
2. **Conditional loading:** Load the JavaScript after the element is defined in the HTML.
3. **Event listeners:** Use event listeners to execute your JavaScript code only after the DOM is fully loaded and the element has been added.