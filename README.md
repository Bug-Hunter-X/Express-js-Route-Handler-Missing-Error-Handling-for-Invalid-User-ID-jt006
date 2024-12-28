# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input parameters.  Specifically, the example shows a route that fetches a user by ID.  If the provided ID is not a valid integer, the code will throw an error, causing the application to fail.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version with proper error handling.

## Bug

The `bug.js` file attempts to parse the user ID as an integer using `parseInt()`, but doesn't check if the result is actually an integer or handle the case where `parseInt()` returns `NaN`. This can lead to unexpected behavior or crashes.

## Solution

The `bugSolution.js` file adds error handling to address this issue.  It checks if `parseInt()` returns `NaN` and sends a 400 Bad Request response if the ID is invalid.