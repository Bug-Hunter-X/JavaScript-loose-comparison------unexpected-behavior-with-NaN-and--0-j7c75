# JavaScript Loose Comparison Bug

This repository demonstrates an unexpected behavior of JavaScript's loose comparison operator (==) when dealing with NaN (Not a Number) and -0 (negative zero).

## The Bug

JavaScript's loose comparison does not work as expected with NaN and -0.  The `==` operator should ideally indicate whether two values are the same.  However, this isn't always true.  

- `NaN` is never equal to itself (`NaN == NaN` evaluates to `false`).
- `-0` is equal to `0` (`-0 == 0` evaluates to `true`).

This behavior can lead to unexpected results in your code if you are not aware of these peculiarities.  The provided `bug.js` file shows how this behavior can lead to unexpected results. 

## The Solution

To handle this correctly, you should use strict comparison (`===`) instead of loose comparison (`==`) whenever possible.   The `bugSolution.js` file demonstrates the solution using strict equality.

Strictly comparing values will result in a more accurate comparison.  This is the suggested and recommended best practice.