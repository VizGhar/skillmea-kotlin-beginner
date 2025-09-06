# 3.5 Higher Functions

## 3.5.1 Foundation

Write the `check` function, which:
1. accepts 3 numbers and a literal
2. returns a `Boolean`
3. with the literal accepting 2 numbers and returning a `Boolean`

The literal in this function calls for pairs _A-B_, _A-C_ and _B-C_

If all literals return `true`, the `check` function also returns `true`

For example, when entering `1 5 7` and literals `a < b` returns our function `true`, because:
1. `1 < 5`
2. `1 < 7`
3. `5 < 7`

Try these options for the literal:
1. A < B
2. A > B
3. A is divisible by B
4. A + B is even
5. A and B end with the same digit