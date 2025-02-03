# React setInterval Memory Leak

This repository demonstrates a common error in React applications: using `setInterval` within a component's `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it fails to include a cleanup function in the `useEffect` hook to clear the interval when the component unmounts.

## Solution

The `bugSolution.js` file provides a corrected version of the component. It includes a cleanup function that calls `clearInterval` to stop the interval when the component unmounts, preventing memory leaks.

## How to reproduce

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the counter in the browser. The buggy version will continue to update even after the component is unmounted, leading to memory leaks. The solution will fix this issue.