# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by incorrect dependency management.

## Bug Description
The `MyComponent` function uses the `useEffect` hook to update the `count` state variable. However, the dependency array `[]` is empty, meaning the effect runs after every render.  This creates a cycle: the effect updates `count`, causing a re-render, which triggers the effect again, leading to an infinite loop and crashing the browser.