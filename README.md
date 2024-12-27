# Unhandled Promise Rejection in Node.js Express Server

This repository demonstrates a common error in Node.js applications: unhandled promise rejections. The example shows an Express.js server that might throw an error during an asynchronous operation. If not handled properly, this will cause the server to crash.

## The Bug

The `bug.js` file contains an Express.js server that simulates an asynchronous operation (using `setTimeout`).  This operation randomly throws an error.  Without proper error handling, this unhandled error will lead to a crash.

## The Solution

The `bugSolution.js` file shows how to handle the error gracefully using a `try...catch` block within the asynchronous operation and a global unhandledRejection event listener to prevent server crashes.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js`.
4. Refresh the page multiple times.  Eventually, the server will crash due to the unhandled error.
5. Run `node bugSolution.js` to see the fixed version.