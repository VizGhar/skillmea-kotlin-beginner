# 2.3 While a Do-while

You can give your application basic logic using the `if` keyword. Let's get started

## 2.3.1 Menu Screen

Many games start with a welcoming menu screen offering options such as:

- [N]ew Game
- [L]oad Game
- [E]xit Game

Write a program that waits until the user enters one of these letters N/L/E. If they enter a correct letter, print which option was chosen and exit the program. If they enter an incorrect letter/text, print an error message and repeat the program.

## 2.3.2 8th Wonder

Warren Buffet called compound interest the 8th wonder of the world. He referred to the increasing rates of return in investments. For example, if you invest 1000EUR with a yield of 10%, that investment will grow as follows:

1. 1000 + 100
2. 1100 + 110
3. 1210 + 121
4. 1331 + 133.1
5. 1464.1 + 146.41
6. ...

Find out how many years it will take for an investor to reach a million from an initial investment of 10000EUR.

## 2.3.3 Do-while

Write a program that generates a random integer between 1 and 10, then repeatedly asks the user to guess this number. The program continues until the user correctly guesses the number. At the end, print how many attempts the user needed.

Here's your starting point:

```kt
import kotlin.random.Random

fun main() {
    val target = Random.nextInt(1, 11) // random integer between 1 and 10

    do {

    } while (true)

    println("Correct! Number of attempts: ???")
}
```

**Condition:** Use a do-while loop to repeat input processing.

## 2.3.4 Number of Ciphers

Read an integer from the standard input into an integer variable. Print how many ciphers it has on the standard output.