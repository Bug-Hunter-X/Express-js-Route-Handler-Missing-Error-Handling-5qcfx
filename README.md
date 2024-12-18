# Express.js Route Handler Missing Error Handling
This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Bug Description
The original code attempts to retrieve a user from an array based on the ID passed in the request parameters. It fails to handle cases where the ID is not a valid number or if a user with the given ID does not exist. This can lead to unexpected errors and crashes.

## Solution
The solution adds robust error handling. It checks if the `userId` can be parsed as an integer and whether a user with that ID exists. If not, it returns an appropriate HTTP status code (404 Not Found) with a clear error message.