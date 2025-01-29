# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: neglecting to handle promise rejections in asynchronous operations.  The `bug.js` file shows an example where an asynchronous operation (`someAsyncOperation`) might fail, but the error is not caught, leading to a silent failure. The solution is provided in `bugSolution.js`

## How to Reproduce

1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Observe that the server might fail silently (if `someAsyncOperation` rejects).
5. Run `node bugSolution.js` to see the correct implementation.

## Solution

The solution involves using `.catch()` to handle potential errors in the promise chain.