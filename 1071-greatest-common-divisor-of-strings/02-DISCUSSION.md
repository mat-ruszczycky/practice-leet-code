# Discussion

- [Leet Code](#FPO)
- [Solutions](./index.html)
- [Problem](./01-PROBLEM.md)

## Approach

1. The function starts by checking if concatenating `str1` and `str2` is equal to concatenating `str2` and `str1`. If this condition is not met, it means that the two strings cannot have a common divisor, and the function returns an empty string "".

2. The lengths of `str1` and `str2` are then stored in variables `n` and `k`, respectively.

3. The function gcds is defined using recursion to calculate the greatest common divisor of two numbers using the Euclidean algorithm. The function `gcds` is defined using recursion to calculate the greatest common divisor of two numbers using the Euclidean algorithm.

4. The GCD of the lengths of `str1` and `str2` is calculated using the `gcds` function.

5. Finally, the function returns a substring of `str1` from index 0 to `div`. This substring represents the longest common prefix of the two strings, which is the result of the GCD calculation.

### Euclidean algorithm 

**Objective:**
Find the greatest common divisor (GCD) of two numbers, which is the largest number that divides both of them.

**Steps:**
1. **Start with two numbers, let's call them \(a\) and \(b\).**
2. **Divide the larger number \(a\) by the smaller number \(b\).**
   - Get the quotient (\(q\)) and the remainder (\(r\)).
   - \(a = b \times q + r\)

3. **Replace \(a\) with \(b\) and \(b\) with \(r\).**
   - Now, \(b\) becomes the new larger number, and \(r\) becomes the new smaller number.
   - Repeat the division.

4. **Continue repeating steps 2 and 3 until the remainder (\(r\)) becomes zero.**
   - The last non-zero remainder is the GCD of the original two numbers.

**In Simple Terms:**
- Keep dividing the larger number by the smaller one.
- Replace the larger number with the smaller one and the smaller one with the remainder.
- Keep doing this until there's no remainder.
- The last non-zero remainder is the GCD.

**Example:**
Let's find the GCD of 48 and 18.
1. \(48 = 18 \times 2 + 12\) (replace 48 with 18 and 18 with 12)
2. \(18 = 12 \times 1 + 6\) (replace 18 with 12 and 12 with 6)
3. \(12 = 6 \times 2 + 0\) (replace 12 with 6 and 6 with 0)

The last non-zero remainder is 6, so the GCD of 48 and 18 is 6.

## Time complexity

The time complexity of the provided JavaScript function primarily depends on the calculation of the greatest common divisor (GCD) using the Euclidean algorithm. The time complexity of the Euclidean algorithm is generally expressed as `O(log(min(x, y)))`, where x and y are the two numbers for which the GCD is being calculated.

In the given code:

```
let gcds = function (x, y) {
    if (!y) {
        return x;
    }
    return gcds(y, x % y);
}
```

The recursive function gcds is called with parameters `x` and `y`. In each recursive call, the value of `y` becomes the remainder of the division of `x` by `y`, and the process continues until `y` becomes zero. The number of recursive calls is logarithmic in relation to the smaller of the two input values (`x` and `y`), resulting in a time complexity of `O(log(min(x, y)))`.

Therefore, the overall time complexity of the provided gcdOfStrings function is dominated by the time complexity of the GCD calculation, and it can be expressed as `O(log(min(n, k)))`, where n and k are the lengths of the input strings `str1` and `str2`, respectively.

## Space complexity

The space complexity of the provided JavaScript function is determined by the space used in the call stack during the recursive GCD calculation and the space required for the additional variables.

Let's break down the main components contributing to the space complexity:

1. **Call Stack**:

    The GCD calculation is implemented using recursion, which involves the use of the call stack to keep track of each recursive call. The space consumed in the call stack is proportional to the depth of recursion.

    The depth of recursion is determined by the number of recursive calls needed to reach the base case. In the case of the Euclidean algorithm, the worst-case depth of recursion is ``O(log(min(x, y)))``.


2. **Additional Variables**:

    The function uses a few additional variables like `n`, `k`, `gcds`, and `div`, but these use constant space and do not depend on the input size.

    Combining these factors, the overall space complexity of the gcdOfStrings function can be expressed as ``O(log(min(n, k)))``, where `n` and `k` are the lengths of the input strings `str1` and `str2`, respectively. This reflects the space consumed by the call stack during the recursive GCD calculation. The additional variables contribute to constant space, so they do not affect the overall asymptotic space complexity.