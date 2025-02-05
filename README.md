# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common error in JavaScript related to closures and the `setTimeout` function within loops.  The issue arises because the `setTimeout` callback function doesn't capture the value of `i` at the time it's created, but rather captures a reference to the variable `i`.  By the time the `setTimeout` callbacks finally execute, the loop has already completed, and `i` holds its final value.

## Bug

The `bug.js` file contains the problematic code. When executed, it prints '10' ten times instead of the expected sequence 0 to 9.

## Solution

The `bugSolution.js` file provides a corrected version using an immediately invoked function expression (IIFE) to create a new scope for each iteration, effectively capturing the correct value of `i`.

This example showcases the importance of understanding closures and how they interact with asynchronous operations in JavaScript.