# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook. The component creates an infinite loop because the useEffect function does not have a dependency array and triggers on every render, logging the count repeatedly. 

## Bug Description
The `useEffect` hook in `MyComponent` lacks a dependency array. As a result, it runs after every render, leading to an infinite render loop and excessive console logging. This can cause performance issues and application crashes.

## Solution
The solution involves providing a dependency array to `useEffect`. The dependency array should contain any values that the effect depends on. In this case, we only need to include the `count` state variable since the effect only needs to log the count.