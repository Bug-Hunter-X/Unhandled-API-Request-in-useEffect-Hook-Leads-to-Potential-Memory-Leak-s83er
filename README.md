# Unhandled API Request in useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook and API requests. The `bug.js` file shows a component that fetches data but doesn't properly clean up the request if the component unmounts before the request completes. This can lead to memory leaks and errors.

The `bugSolution.js` file provides a corrected version that uses the `AbortController` API to cancel the request on unmount, preventing these issues.  This is crucial for robust and efficient React applications.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console for errors or warnings (you might need to simulate a quick unmount to see effects).

## How to solve the bug

The solution demonstrates the best practice of using `AbortController` to cancel the fetch requests, preventing any memory issues. Carefully examine the use of cleanup functions in useEffect hooks when making API calls.