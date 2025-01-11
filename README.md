# React 19 useEffect Cleanup Issue

This repository demonstrates a common error in React 19 related to the `useEffect` hook when using `setInterval`. Forgetting to return a cleanup function from `useEffect` leads to memory leaks and unexpected behavior. 

## The Bug
The `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook without proper cleanup. This results in the `setInterval` continuing to run even after the component is unmounted, causing memory leaks. 

## The Solution
The `bugSolution.js` file demonstrates the corrected code. It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, resolving the memory leak issue.