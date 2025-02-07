# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Problem

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks the necessary cleanup function to stop the interval when the component unmounts.

## Solution

The `bugSolution.js` file shows the corrected version.  It uses the returned function from `setInterval` within the cleanup function of `useEffect` to stop the interval when the component is no longer needed.