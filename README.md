# Lua Nested Table Iteration Bug

This repository demonstrates a common error encountered when iterating over nested tables in Lua using the `pairs` function. The `pairs` iterator does not guarantee any specific order, which can lead to unexpected behavior if you modify the table during iteration.  This example showcases how a seemingly harmless nested function call can cause unexpected issues.

## Bug Description
The `foo` function recursively iterates through a nested table. While the intention is to process all elements, the lack of order in `pairs` can lead to unexpected results. The print statement might not output the expected value because the table structure might change unexpectedly due to the order of iteration.

## Solution
The solution illustrates using a different approach to iterate the table, ensuring consistent results.