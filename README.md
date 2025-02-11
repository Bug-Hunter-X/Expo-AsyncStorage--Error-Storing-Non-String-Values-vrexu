# Expo AsyncStorage: Non-String Value Error

This repository demonstrates a common error encountered when using AsyncStorage in Expo applications: attempting to store a non-string value.  AsyncStorage in Expo only accepts strings. Attempting to store other data types (like objects, numbers, or booleans) results in unexpected behavior and a cryptic error message.

The `bug.js` file shows the problematic code, while `bugSolution.js` demonstrates the correct approach.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run the app and observe the error behavior in `bug.js`.
4. Examine `bugSolution.js` for the corrected implementation.

## Solution

Always convert your data to a string before storing it in AsyncStorage using methods like `JSON.stringify()`.  Similarly, parse the data back using `JSON.parse()` after retrieval.