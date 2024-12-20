# React Native Unhandled JS Exception: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common React Native error: attempting to access a state variable before it's been initialized. This typically occurs when rendering a component that relies on asynchronous data fetching before the data has arrived.

## Problem
The `bug.js` file shows a component that fetches data.  It attempts to render the fetched data immediately, resulting in an error because `this.state.data` might be `null` or `undefined` initially.

## Solution
The `bugSolution.js` file presents a corrected version. It uses a conditional rendering approach, displaying a loading indicator or fallback message while the data is fetched, and then displays the data once it's available.  This prevents trying to access `this.state.data` before it's ready.

## How to reproduce
1. Clone this repo.
2. Navigate to the directory.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the error in the original file, then see the corrected behavior in the solution file. 