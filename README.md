# React setInterval Cleanup Issue

This repository demonstrates a common React bug involving the improper use of `setInterval` within the `useEffect` hook, leading to memory leaks.  The `bug.js` file contains the flawed code, while `bugSolution.js` provides the corrected version.

## Problem

The original component uses `setInterval` to update the count every second. However, it lacks a cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing to run indefinitely, even after the component is no longer displayed, leading to a memory leak.

## Solution

The solution involves using the cleanup function provided by `useEffect` to call `clearInterval` before the component unmounts. This ensures that the interval is properly stopped, preventing memory leaks and improving the overall performance of the application.