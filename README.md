# React Router Dom Wildcard Route `/*` Issue

This repository demonstrates a common issue encountered when using wildcard routes (`/*`) in React Router DOM v6.  The wildcard route unintentionally captures all paths, preventing other routes from working correctly.  The solution provides a workaround for this problem.

## Problem

The provided `App.js` file shows a standard React Router setup with routes for `/`, `/about`, and a wildcard route `/*`. The expectation is that `/*` would only match when no other route matches; however, this is not what happens.  The wildcard route always matches, regardless of the URL.

## Solution

The solution is to move the wildcard route to the end of the routes list in the `Routes` component.  By ordering the routes this way, the more specific routes are checked first, which effectively solves the issue.