# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook that can lead to an infinite loop.  The issue stems from improperly managing state updates within the effect's callback. The `useEffect` hook is used incorrectly in the initial example to reset the count which leads to unexpected and undesirable behavior.

## Problem

The provided code has an `useEffect` hook that attempts to reset the counter when it exceeds 5. However, this implementation creates an infinite loop because each update to the `count` state triggers a re-render, and the effect runs again, causing another state update and hence another re-render and so on.