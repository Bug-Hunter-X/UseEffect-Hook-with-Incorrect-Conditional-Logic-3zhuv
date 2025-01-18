# React useEffect Hook Bug

This repository demonstrates a common error when using the `useEffect` hook in React. The bug lies in the conditional logic within the `useEffect` function. The condition `count > 5` is only checked once, after the component mounts, and will not correctly update as the count changes.

## Bug Description
The provided code implements a simple counter component using `useState` and `useEffect`. The `useEffect` hook is intended to log messages to the console based on whether the `count` is greater than 5. However, due to improper handling of the `count` variable within the `useEffect` dependency array, the condition is only evaluated once, which is incorrect.

## Solution
The solution corrects this by ensuring the `useEffect` is called whenever `count` changes. This ensures that the log messages are displayed in the console correctly.