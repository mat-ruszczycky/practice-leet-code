# Discussion

- [Leet Code](https://leetcode.com/problems/merge-strings-alternately/description/?envType=study-plan-v2&envId=leetcode-75)
- [Solutions](./index.html)
- [Problem](./01-PROBLEM.md)

## Approach

Both `mergeAlternately1` and `mergeAlternately2` functions aim to merge two strings alternately, taking characters from each string in turn until the end of either string is reached. Below are the key steps for each function:

### `mergeAlternately1`:

1. **Initialization**:

- Initialize an empty string (`result`) to store the merged `result`.

2. **Iteration**:

- Iterate through the characters of the longer of the two words using a for loop.
- Append the current character from `word1` to the `result` if there are characters remaining in `word1`.
- Append the current character from `word2` to the `result` if there are characters remaining in `word2`.

3. **Concatenation**:

- Return the merged result.

### `mergeAlternately2`:

1. **Initialization**:

- Initialize variables (`lenW1`, `lenW2`, `i`, and `word`) to store the lengths of words and an empty array to store the merged characters (`word`).

2. **Iteration**:

- Use a while loop to iterate through the characters of both `words` until the end of either `word` is reached.
- Push the current characters from both words alternately into the `word` array.

3. **Remaining Characters Handling**:

- If there are remaining characters in `word1`, concatenate them to the result using `Array.concat()` and `Array.join()`.
- If there are remaining characters in `word2`, concatenate them to the result using the same approach.

4. **Equal Length Handling**:

- If both words are of equal length, join the characters alternately and return the result.

## Time complexity

### Solution 1

The time complexity of the provided `mergeAlternately1` function is `O(max(N, M))`, where `N` is the length of `word1` and `M` is the length of `word2`. This is because the function iterates through the characters of the longer of the two words, where `N` and `M` represent the lengths of `word1` and `word2`, respectively. The loop runs for a number of iterations equal to the length of the longer word.

In the worst case, where the lengths of `word1` and `word2` are equal, the time complexity simplifies to `O(N)`, where `N` is the length of either `word1` or `word2`.

The operations inside the loop (appending characters to the result string) are constant time operations, and they do not change the overall time complexity. Therefore, the dominant factor in determining the time complexity is the length of the longer word.

### Solution 2

The time complexity of the provided `mergeAlternately2` function is `O(min(N, M))`, where `N` is the length of `word1` and `M` is the length of `word2`. This is because the function iterates through the characters of both words until the end of either `word1` or `word2`.

In the worst case, where one of the words is significantly shorter than the other, the time complexity will be determined by the length of the shorter word. The loop runs for a number of iterations equal to the length of the shorter word.

The operations inside the loop (pushing characters to the word array) and the final concatenation and joining steps involve constant time operations. Therefore, the dominant factor in determining the time complexity is the length of the shorter word.

In scenarios where the lengths of `word1` and `word2` are equal, the time complexity simplifies to `O(N)` or `O(M)`, where `N` and `M` are the lengths of `word1` and `word2`, respectively.

## Space complexity

In both functions, the space complexity is determined by the length of the merged result, which is proportional to the sum of the lengths of `word1` and `word2`. The other variables and data structures used in the functions contribute only a constant amount of space.

### Solution 1

The primary space used is for the result string, which accumulates the merged characters. The length of this string is the sum of the lengths of `word1` and `word2`. Therefore, the space complexity is `O(N + M)`, where `N `is the length of `word1` and `M` is the length of `word2`.

### Solution 2

The primary space used is for the word array, which accumulates the merged characters. The length of this array is at most the sum of the lengths of `word1` and `word2`. Additionally, there is a constant amount of space used for variables `lenW1`, `lenW2`, `i`, and `word`.

The space complexity is `O(N + M)`, where `N` is the length of `word1` and `M` is the length of `word2`.