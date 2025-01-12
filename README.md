# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook.  The effect runs on every render due to the absence of a dependency array, leading to unnecessary work and potential performance problems. The solution shows how to fix this by correctly specifying the dependencies.

## Bug
The `bug.js` file contains the problematic code. The `useEffect` hook doesn't have a dependency array, causing it to run after every render, including state changes that it doesn't actually depend on. 

## Solution
The `bugSolution.js` file demonstrates the correct usage. By adding the `count` variable to the dependency array, `useEffect` only runs when the `count` value changes. This significantly improves the efficiency of the component.