# 6.2 Polia

## 6.2.1 Single-Dimensional Array

### Input
1. Read an integer `n`
2. Read `n` lines with integers each
3. Read two integers `k` and `m`

### Output
Replace all values equal to `k` in the input array with `m`.

## 6.2.2 Matrix Addition

A two-dimensional array is simply an array of arrays. One way a two-dimensional array can look like this:

```kt
val pole1 = arrayOf(
    arrayOf(1, 2),
    arrayOf(3, 4),
    arrayOf(5, 6)
)
```

### Input
1. Read the height `h` and width `w` of the 2D array
2. `h` x `w` values representing the first 2D array
3. `h` x `w` values representing the second 2D array

### Output
Print the result of adding these two matrices.

| Example Input | Example Output |
|--------------|----------------|
| ```2 2```<br/>```1 2```<br/>```3 4```<br/>```7 3```<br/>```2 8```         | ```8 5```<br/>```5 12```            |
| ```2 4```<br/>```1 2 15 5```<br/>```13 6 21 8```<br/>```3 2 8 8```<br/>```9 18 5 22``` | ```4 4 23 13```<br/>```22 24 26 30``` |

## 6.2.3 Map Editor

Create a simple editor for a 2D ASCII game.

1. Read the size of the playing field from standard input. The default character on this field is `.`.
2. Loop
   1. Read `X` and `Y` coordinates where you want to place an object
   2. Read `symbol`, which you want to place at position `[X, Y]`
   3. Draw the map so far


| Example Input | Example Output (only last iteration) |
|--------------|---------------------------------------|
| ```3 3```<br/>```0 0 /```<br/>```2 0 \ ```<br/>```0 2 \ ```<br/>```2 2 /``` | ```/.\ ```<br/>```...```<br/>```\./``` |