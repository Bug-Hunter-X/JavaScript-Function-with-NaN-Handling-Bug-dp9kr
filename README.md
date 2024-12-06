# JavaScript Function with NaN Handling Bug

This repository demonstrates a subtle bug in a JavaScript function that deals with null and NaN values. The function `foo` aims to add two numbers, handling null inputs gracefully. However, it does not explicitly handle NaN values, which can lead to unexpected behavior. 

## Bug Description

The `foo` function correctly handles null inputs by returning 0.  The problem is that it doesn't handle NaN values, which can arise from various arithmetic operations (e.g., `parseInt("abc")`). When NaN is encountered the result of `a + b` will be NaN.  This could be problematic if the calling code doesn't expect NaN as a result.

## Solution

The solution adds a check for NaN values.  If either input is NaN, the function now returns 0, thereby giving consistent behavior for null and NaN inputs.  This prevents unexpected results and improves robustness.