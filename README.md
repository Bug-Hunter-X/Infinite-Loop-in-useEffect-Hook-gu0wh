# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from improperly specifying the dependency array, leading to an infinite render loop.

## Bug Description
The `useEffect` hook in `bug.js` is intended to log the current count to the console after each render.  However, the absence of the `count` variable in the dependency array causes the effect to run on every render, triggering a new state update, and creating an infinite loop. 

## Solution
The solution, found in `bugSolution.js`, correctly includes `count` in the dependency array.  This ensures the effect only runs when the `count` value changes.