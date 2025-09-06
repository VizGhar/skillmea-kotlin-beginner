# 3.1 Functions - Fundamentals

You can test basic function forms in Kotlin on practical tasks. Functions usually process inputs into outputs, but there are more writing styles.

Tasks will require only writing functions. You should write your own test code, of course.

## 3.1.1 No Input and Output

Write a function called `menu` that prints the main menu content to standard output according to task [2.3.1 Menu Screen](../02-code-branching/02-03-while_and_do_while.MD). This function is only for printing, so it will be small.

## 3.1.2 With Input, No Output

Write a function that takes two whole numbers as input to represent a 2D space. According to conditions described in task [2.5.3 Boundary checker](../02-code-branching/02-05-logic_operators.MD), loop through coordinates `x` and `y` until all conditions are met.

When the conditions are met, print:
> Coordinate is `[x, y]`

## 3.1.3 No Input with Output

Write a function called `readPrime` whose task is to read a prime number from standard input. This function should not return any number except a prime number (will contain a cycle with validation).

## 3.1.4 No Input with Output 2

Write a function called `consoleReadYn` whose task is:
1. Print text `Do you want to continue? [Y/n]`
2. Return `true` if the input text is `Y` or `y`
3. Return `false` if the input text is not `Y` or `y`

## 3.1.5 With Input and Output

Modify task 3.1.2. Pass width, height, x, and y coordinates to the function. The function should return `true` if x and y are within a space defined by height and width. Move the cycle for verifying input into the main function, for example:

```kt
fun main() {
    // ... get width, height
    while(true) {
        // ... get x, y
        if (isValid(width, height, x, y)) {
            // output
            break
        }
    }
}
```