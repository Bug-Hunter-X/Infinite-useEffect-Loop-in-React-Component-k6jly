# Infinite useEffect Loop in React

This repository demonstrates a common React error: an infinite useEffect loop caused by a missing dependency array. The component continuously re-renders, leading to performance degradation and excessive console logging.

## Problem

The `useEffect` hook in `bug.js` lacks a dependency array.  This means it runs after every render, creating a cycle: the effect updates the state, triggering a re-render, which in turn triggers the effect again.

## Solution

The `bugSolution.js` file corrects this by including `[count]` as a dependency array. Now, the effect only runs when the `count` state variable changes.