# 5.1 Chance

Let's take a look at how we can work with random values in Kotle.

## 5.1.1 Guess the number

1. The application will generate a random number `k` from the interval 1-100 upon startup.
2. Display the text: _"Guess which number I'm thinking of 0-100:"_
3. Until the user correctly guesses the number
   1. Read a number `c` from standard input
   2. If `c` is less than `k`, display: _"higher"_ 
   3. If `c` is greater than `k`, display: _"lower"_ 
   4. If `c` equals `k`, display: _"correct"_ and terminate the cycle

## 5.1.2 Random text

Random does not provide functions for generating texts. Try writing your own function to generate a random text.

You might want to take a glance at [ASCII tables](https://www.ascii-code.com/) to remind yourself which numbers represent which character.