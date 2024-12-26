# F# Mutable Variable Swap Bug

This example demonstrates a common error when working with mutable variables in F#. The `swap` function attempts to swap the values of `x` and `y`, but it doesn't work as expected.

## Bug Description
The issue lies in how F# handles mutable variables within functions.  The `swap` function modifies the local copies of `x` and `y` within its scope, but these changes do not affect the variables `x` and `y` in the outer scope.

## Solution
To fix this issue, we can return the swapped values from the `swap` function and reassign them to `x` and `y`.