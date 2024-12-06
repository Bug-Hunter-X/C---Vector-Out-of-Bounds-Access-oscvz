# C++ Vector Out-of-Bounds Access Bug

This repository demonstrates a common C++ error: accessing an element beyond the bounds of a `std::vector`.  The provided code attempts to iterate through the vector using an index that goes beyond the valid range, resulting in undefined behavior.

## Bug Description
The bug lies in the loop condition used to iterate through the vector.  The loop continues as long as `i` is less than or equal to the size of the vector. Since vector indices are zero-based, the last valid index is `vec.size() - 1`. Accessing `vec[vec.size()]` will lead to undefined behavior, often resulting in a program crash or unexpected results.

## Solution
The solution is to modify the loop condition to iterate only up to `vec.size() - 1` (or use iterators for safer iteration).