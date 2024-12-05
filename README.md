# Uncommon HTML Bug: innerHTML and DOM Node Concatenation

This repository demonstrates an uncommon bug in HTML that arises from incorrectly using innerHTML to add a DOM node to the existing content. The bug occurs when trying to concatenate a string with a DOM Node using the '+' operator within the innerHTML assignment.  innerHTML only accepts strings. Attempting to use a DOM Node in this context results in an unexpected behavior; the node is not added. This example showcases this problem and provides a solution.

## Bug Description
The bug lies in the JavaScript code that attempts to append a new paragraph element to an existing div using innerHTML.  Directly concatenating a created `<p>` element with a string within the innerHTML assignment is invalid. This leads to only the string part being rendered, and the new paragraph is lost.

## Solution
The solution involves creating the paragraph element and then appending it to the div using the `appendChild()` method, which is the correct approach for adding DOM elements.