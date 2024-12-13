# React Router v6 Catch-All Route Issue

This repository demonstrates an unexpected behavior with the catch-all route ("/*") in React Router v6 when nested within other routes. The catch-all route is triggered even when a more specific route matches.

## Bug

The issue occurs when a catch-all route is placed within the `Routes` component.  Regardless of the path, the catch-all route is activated, overriding any other route. The provided `App.js` shows the problematic code.

## Solution

The solution involves restructuring the routes. The catch-all route should always be placed as the last route in the `Routes` component to ensure it only catches unmatched paths. The solution is demonstrated in `AppSolution.js`.