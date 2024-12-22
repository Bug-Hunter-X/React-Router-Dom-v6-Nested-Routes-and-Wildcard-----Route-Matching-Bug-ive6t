# React Router Dom v6 Nested Routes and Wildcard (*) Route Matching Bug

This repository demonstrates a bug in React Router Dom v6 related to unexpected route matching behavior when using nested routes and wildcard (*) routes.  The wildcard route unexpectedly matches all paths, including those that should be matched by other, more specific routes.

## Problem

When a wildcard route is present within a nested route structure, it will prevent other nested routes from matching. This occurs even if the more specific routes should match the given path.

## Solution

The solution involves carefully ordering routes and using the `index` element of the routes when needed to make sure more specific routes match before more generic ones.  The wildcard route should generally be the very last route defined.