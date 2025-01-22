# React Router Catch-All Route Conflict

This repository demonstrates a common issue with React Router's catch-all route (`/*`).  When placed before other routes, it intercepts all navigation attempts, preventing access to other routes.

The solution involves moving the catch-all route to the end of the `Routes` component to ensure it only matches when no other route matches.

## Bug

The `App.js` file contains the buggy code.  Navigating to `/about` will still show the 404 page because the catch-all route intercepts the path before other routes can be matched.

## Solution

The `AppSolution.js` file demonstrates the corrected code with the catch-all route placed at the end of the `Routes` component.