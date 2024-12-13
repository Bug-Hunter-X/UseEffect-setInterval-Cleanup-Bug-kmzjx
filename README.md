# React useEffect setInterval Cleanup Bug

This repository demonstrates a common bug in React components involving the use of `setInterval` within the `useEffect` hook without proper cleanup.  Failure to clear the interval leads to memory leaks and unexpected behavior.

## Bug Description

The `MyComponent` attempts to update a counter every second using `setInterval`. However, it lacks a cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing to run indefinitely, even after the component is no longer needed, leading to memory leaks and potential performance issues.

## Solution

The solution involves adding a cleanup function to the `useEffect` hook that uses `clearInterval` to stop the interval before the component is unmounted.