# 2.5 Logical Operators

You can use logical operators to combine two `if` statements into one!

## 2.5.1 Test ||

On standard input, read a number `n` (`n < 1000`). Print all numbers less than `n` that are divisible by 5 or 11.

## 2.5.2 Test &&

On standard input, read a number `n` (`n < 1000`). Print all numbers less than `n` that are divisible by 5 and also have at least one three in their tens digit.

## 2.5.3 Boundary Checker

On standard input, read the width `width` and height `height` of a 2D space. Then, repeatedly read values `x` and `y`.

The starting point in this 2D space has coordinates `[0, 0]`

1. If a point at coordinates `[x, y]` is outside the 2D space, print an error message
2. If a point at coordinates `[x, y]` is within the 2D space, print a success message

_Example inputs and outputs:_
```
5 4        // width is 5, height is 4
0 0 OK     // 0 0 falls within the bounds <0, 5] and <0, 4]
5 0 CHYBA  // x does not fall within the bounds <0, 5]
0 4 CHYBA  // y does not fall within the bounds <0, 4]
3 3 OK     //
-1 0 CHYBA // x does not fall within the bounds <0, 5]
```