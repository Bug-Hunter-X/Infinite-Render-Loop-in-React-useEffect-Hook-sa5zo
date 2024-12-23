# React Infinite Render Loop Bug

This repository demonstrates a common React bug: an infinite render loop caused by improperly using the `useEffect` hook.  The `bug.js` file contains the erroneous code. The `bugSolution.js` file provides the corrected code.

The issue stems from updating the state variable `count` within the `useEffect` hook's callback function without a dependency array condition that prevents infinite loops.  This creates a feedback loop where the component constantly re-renders, leading to performance issues and potentially application crashes.

The solution involves modifying the dependency array for the useEffect function, ensuring the effect only runs once during initial render or using a conditional check within the effect to prevent an infinite loop. 