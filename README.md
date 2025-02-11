# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common mistake in using the React `useEffect` hook: forgetting to include a cleanup function.  The example shows a component that logs a message to the console when it mounts, but it fails to remove this listener or perform any cleanup, which can lead to memory leaks and other issues.  The solution demonstrates how to correctly use a cleanup function for proper memory management.

## Bug

The `bug.js` file contains a component with an `useEffect` hook that doesn't have a return statement with a cleanup function. This can lead to memory leaks and other issues if the component is unmounted before the effect is done. 

## Solution

The `bugSolution.js` file demonstrates the corrected code.  The addition of a return function within the `useEffect` hook ensures any resources acquired within the effect are properly released when the component is unmounted, preventing memory leaks.