# Practice Leet Code

Repo for tracking solutions and explanations to leet programs

https://gist.github.com/luismts/495d982e8c5b1a0ced4a57cf3d93cf60
https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13
https://www.markdownguide.org/basic-syntax/

## Complexity

Determining the time and space complexity of an algorithm involves analyzing how the algorithm's performance scales with the input size.

### Time Complexity

1. **Identify Basic Operations:**
   - Examine the operations performed in the algorithm.
   - Identify the dominant operations that contribute the most to the overall runtime.

2. **Count the Operations:**
   - Express the number of basic operations in terms of the input size.
   - Ignore constants and focus on the growth rate concerning the input size.

3. **Big O Notation:**
   - Determine the upper bound of the growth rate using Big O notation.
   - Choose the most significant term in the expression, and drop constants.

   Example:
   - If an algorithm performs a constant number of operations for each element in an array of size 'n', it may be O(n).

### Space Complexity

1. **Identify Memory Usage:**
   - Look at the variables, data structures, and memory allocations used by the algorithm.
   - Identify the space used as a function of the input size.

2. **Count the Memory Usage:**
   - Express the space used in terms of the input size.
   - Consider temporary variables, arrays, and data structures.

3. **Big O Notation for Space:**
   - Determine the upper bound of the space growth rate using Big O notation.
   - Choose the most significant term in the expression and drop constants.

   Example:
   - If the space used by an algorithm scales linearly with the input size, it may have a space complexity of O(n).

### Common Time and Space Complexities

- O(1): Constant time or space complexity.
- O(log n): Logarithmic time complexity (common in binary search).
- O(n): Linear time or space complexity.
- O(n log n): Log-linear time complexity (common in efficient sorting algorithms).
- O(n^2): Quadratic time complexity.
- O(2^n): Exponential time complexity.
- O(n!): Factorial time complexity.

### Tips

- **Focus on Dominant Terms:** In both time and space complexity, focus on the dominant terms that have the most significant impact on performance.

- **Ignore Constants:** Big O notation abstracts away constants, so focus on the general growth rate.

- **Consider Worst Case:** Analyze the worst-case scenario for the algorithm, as it provides an upper bound on its performance.

- **Use Iteration and Recursion:** For loops, analyze the number of iterations. For recursive algorithms, use recurrence relations.