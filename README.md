# React useEffect Dependency Array Bug
This repository demonstrates a common bug in React related to the useEffect hook and its dependency array.  The bug causes unexpected re-renders and potential performance issues. The solution shows how to correctly manage the dependency array to prevent the bug.

## Bug Description
The original code has a `useEffect` hook without properly specifying the dependency array.  This leads to unintended re-renders every time the component updates which can severely affect performance and often lead to difficult-to-debug infinite loops. 

## Solution
The solution correctly specifies the dependency array.  By only including the variable that causes changes, we eliminate unnecessary rerenders. In this case, only including `count` ensures that the effect only runs when the count changes.