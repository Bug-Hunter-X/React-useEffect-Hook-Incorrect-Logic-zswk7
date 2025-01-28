# React useEffect Hook Incorrect Logic

This example demonstrates a common error in React's `useEffect` hook where the logic for updating state is flawed, leading to unexpected behavior. The initial intention was to set the `count` state to 10 only once when the component mounts. However, due to the incorrect condition within the `useEffect`, the state will not update on subsequent clicks. 

## Bug

The provided code updates the count to 10 only on component mount.  Clicking the increment button does not change the count beyond 10 if it was initially 0. If the initial state is not 0, the count will not change at all.

## Solution

The solution removes the conditional update, allowing the `setCount` function to update the count correctly whenever the button is clicked.