# React useEffect Hook with Missing Dependencies

This repository demonstrates a common issue in React applications: an improperly used `useEffect` hook that leads to unexpected re-renders and potentially infinite loops.

## Problem

The `useEffect` hook, without the correct dependency array, runs after every render instead of only when the specified dependencies change.  This causes unexpected behavior, especially when the effect modifies state that triggers re-renders. 

## Solution

The solution involves properly specifying the dependencies in the dependency array. In this case, the dependency array should include only `count`. This ensures the effect only runs when the `count` changes.