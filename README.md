# React Infinite Loop in useEffect Hook

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook. The problem arises from incorrectly handling the dependency array and performing actions within the effect that trigger a re-render.

## Bug Description
The `MyComponent` attempts to log the count and increment it within the `useEffect` hook.  However, since `count` is in the dependency array, any change to `count` causes the `useEffect` to run again, creating an infinite loop.

## Solution
The solution involves removing the `setCount` call from within the `useEffect` hook and managing state updates within the component's event handlers.