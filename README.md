# React Native useContext Hook Returns Undefined

This repository demonstrates a common yet tricky error in React Native applications:  The `useContext` hook returning `undefined` even when the context appears to be correctly set up. This often leads to silent failures or unexpected application behavior.

## Problem
The `useContext` hook in React Native is used to access values from a React context. When this hook returns `undefined`, it usually means the context provider isn't correctly wrapped around the component trying to access it, or that there is a problem in the context's rendering hierarchy. The error isn't always immediately obvious as it might not be flagged by the compiler or as a typical type error.

## Solution
Carefully review the context's provider and component tree structure. Ensure the provider is a direct ancestor of the component using `useContext`. Also, check for any issues with context updates and conditional rendering that might affect access.

## Files
- `bug.js`: Demonstrates the problematic code.
- `bugSolution.js`:  Shows the corrected version.