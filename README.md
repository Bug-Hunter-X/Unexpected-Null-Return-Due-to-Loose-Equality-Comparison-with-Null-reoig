# Unexpected Null Return Due to Loose Equality Comparison with Null

This repository demonstrates a common JavaScript error involving loose equality (==) comparisons with null values, leading to unexpected null returns.

## The Bug

The `foo` function intends to add two numbers. However, it uses loose equality (`==`) to check for null values. This leads to the function returning null even when only one of the inputs is null, because `null == 0` evaluates to false.  Strict equality (`===`) should be used instead for accurate null checks. 

## The Solution

The solution replaces loose equality (`==`) with strict equality (`===`) to ensure that only actual null values are handled correctly, preventing unintended null returns. 

## How to reproduce

1. Clone this repository.
2. Navigate to the root directory.
3. Run `node bug.js` to see the buggy behavior.
4. Run `node bugSolution.js` to see the corrected behavior.