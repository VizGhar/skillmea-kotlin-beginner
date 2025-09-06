# 2.4 Break a Continue

`break` and `continue` allow us to terminate or skip the current iteration of a loop.

## 2.4.1 Breakable Menu Screen

Modify the solution from the task [2.3.1 Menu Screen](02-03-while_and_do_while.md) so that instead of using a condition in the `while` loop header, you use `break`

## 2.4.2 Sorter

On standard input, read numbers repeatedly.
1. If no number is entered, print an error message and `break` the cycle
2. If the entered number is odd, call `continue`
3. If the entered number is even, print it to the standard output

## 2.4.3 Primes

Write a program that reads an integer `n` and determines whether it is a prime number.

That is, iterate over numbers `$i \in [2, n-1]$. If the number `n` is divisible by one of the numbers `i`, then `n` is not a prime number.