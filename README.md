# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook:  forgetting to include dependencies in the dependency array.  This can lead to infinite re-renders, crashing the application.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides the corrected code.

## Bug Description
The `useEffect` hook is used to perform side effects after the component renders.  However, if you don't specify the correct dependencies, the effect will run on every render, potentially creating an infinite loop. In this example, the `count` variable is not included in the dependency array, so the effect runs repeatedly.