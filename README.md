# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file shows the corrected version.

## Description
The original code has an infinite loop because the `useEffect` hook doesn't specify `count` as a dependency.  It runs after every render, causing a re-render and another execution, etc.

## Solution
Adding `count` to the dependency array ensures that the effect only runs when `count` changes.