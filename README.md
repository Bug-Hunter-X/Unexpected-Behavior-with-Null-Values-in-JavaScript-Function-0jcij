# JavaScript Null Handling Bug

This repository demonstrates a common error in JavaScript:  assuming the type of function arguments without explicitly checking.  The `foo` function handles null values correctly by returning 0. However, it silently fails to account for situations where the input arguments aren't numbers. This can result in unexpected behavior or runtime errors.

## Bug

The `bug.js` file contains the problematic code.  The function `foo` is vulnerable because it doesn't validate that its input `a` and `b` are numbers before performing arithmetic.  The program will run without crashing but return incorrect results if the inputs aren't numbers.

## Solution

The `bugSolution.js` file provides a corrected implementation.  This version includes a type check using `typeof` to ensure that both `a` and `b` are numbers before performing addition. If either is not a number, it explicitly handles the case.

## How to Run

1. Clone the repository.
2. Navigate to the repository directory in your terminal.
3. Run `node bug.js` to see the original buggy behavior.
4. Run `node bugSolution.js` to see the fixed implementation.