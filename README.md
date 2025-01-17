# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by an incorrectly used `useEffect` hook. 

## Bug Description

The `useEffect` hook in `bug.js` lacks a dependency array. This means that the effect runs after every render, leading to an infinite loop.  Every time the component renders, the `console.log` statement executes and triggers another render, causing the browser to become unresponsive. 

## Solution

The solution, shown in `bugSolution.js`, fixes this by adding an empty dependency array `[]`. This ensures that the effect only runs once after the initial render.