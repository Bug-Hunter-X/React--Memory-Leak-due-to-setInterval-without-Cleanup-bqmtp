# React: Memory Leak due to setInterval without Cleanup

This example demonstrates a common error in React applications: using `setInterval` without proper cleanup in the `useEffect` hook.  This leads to memory leaks as the interval continues to run even after the component unmounts.

## Problem

The `setInterval` function, used to update a counter, lacks a cleanup function within the `useEffect` hook. This means that the interval keeps running indefinitely.  When the component unmounts, the interval continues, causing a memory leak.

## Solution

The solution involves returning a cleanup function from the `useEffect` hook. This function clears the interval when the component unmounts, preventing the memory leak. 
