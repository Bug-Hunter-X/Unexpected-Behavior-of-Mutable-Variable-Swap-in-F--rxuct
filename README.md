# Unexpected Behavior of Mutable Variable Swap in F# 

This example demonstrates a common misconception when working with mutable variables and function arguments in F#. The `swap` function doesn't modify the original variables `x` and `y` as intended because F# passes arguments by value, creating copies within the function's scope. 

## Bug Description:
The provided F# code attempts to swap the values of `x` and `y` using mutable variables. The swap function modifies the local copies of these variables within its scope, leaving the original variables unchanged. 

## Solution:
The bug can be fixed by passing the variables by reference using the `byref` keyword or by using a different approach that avoids mutable variables altogether, which is generally preferred in functional programming.