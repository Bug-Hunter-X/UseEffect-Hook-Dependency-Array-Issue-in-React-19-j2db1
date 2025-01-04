# React 19 useEffect Hook Dependency Array Issue

This repository demonstrates a common issue related to the `useEffect` hook in React 19.  Improper management of the dependency array can lead to unexpected re-renders and potential performance problems. The example shows how forgetting to include state variables in the dependency array can create an infinite loop.

## Bug Description

The `useEffect` hook is designed to perform side effects after every render.  However, if the dependency array is missing crucial state variables, the effect will trigger even when those variables haven't changed, leading to unnecessary re-renders and potentially an infinite loop.

## Solution

The solution involves carefully reviewing the dependency array to ensure that all variables used within the effect are included in the array.  This ensures that the effect only runs when those variables actually change.