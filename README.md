# LeetCode 241 - Different Ways to Add Parentheses

## Problem

Given a string `expression` containing numbers and the operators `+`, `-`, and `*`, return all possible results from computing the expression with different possible ways to add parentheses.

The results can be returned in any order.

## Example

### Input

```text
expression = "2-1-1"
```

### Output

```text
[0,2]
```

The possible calculations are:

```text
(2-1)-1 = 0
2-(1-1) = 2
```

## Approach

Use recursion and divide the expression at every operator.

For each operator:

1. Calculate all possible results from the left side.
2. Calculate all possible results from the right side.
3. Combine every left result with every right result using the current operator.

If the expression contains no operator, it is simply a number.

Memoization is used to avoid calculating the same sub-expression multiple times.

## Algorithm

1. Create a memoization dictionary.
2. For each operator in the expression, split the expression into two parts.
3. Recursively calculate all possible results for both parts.
4. Combine the results according to the operator.
5. If no operator exists, return the number itself.
6. Store the results in the memo dictionary.
7. Return all possible results.

## Complexity

* Time Complexity: Depends on the number of possible results and sub-expressions.
* Space Complexity: `O(n)` for recursion and memoization, excluding the output.

## Language

Python

## LeetCode

Problem: 241 - Different Ways to Add Parentheses

## Author

**T.Nandhini**
