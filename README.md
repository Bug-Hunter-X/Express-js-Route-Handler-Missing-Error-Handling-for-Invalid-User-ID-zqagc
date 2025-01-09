# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  Specifically, the code attempts to parse a user ID as an integer without checking if it's a valid number. This can lead to unexpected behavior or crashes.

## Bug

The `bug.js` file contains the problematic code.  It fetches a user by ID, but doesn't handle cases where the ID is not a valid integer, resulting in a potential error.

## Solution

The `bugSolution.js` file provides a corrected version.  It includes checks to ensure the user ID is a number before attempting to parse it, preventing potential errors.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js`.  Attempt to access a route with a non-numeric ID (e.g., `/users/abc`).
4. Observe the error.
5. Run `node bugSolution.js`. The improved error handling will prevent the crash.