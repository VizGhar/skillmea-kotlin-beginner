# Standard Input and Output

What will mainly concern us is reading from the standard input. I recommend reviewing both tasks when you complete _1.5 String templates_

## 1.4.1 Interactive Greeting

Sometimes, you'll encounter interactivity in console applications, where the application communicates with you. For example, when calling `sudo apt-get upgrade` (Ubuntu), the `apt-get` program may ask:

```
Do you want to continue? [Y/n]
```

The cursor will remain on this line and wait for a key press of `Y` or `n`. After entering the program continues.

Try creating a similar interactive application:

1. Print text: _"Enter your name: "_, with the cursor remaining after that text
2. Read in the _name and surname_ into one variable named `name`
3. Print text: _"Welcome `name`"_, where `name` is the value of the variable from step 2

## 1.4.2 Trap

1. On the first line, read in two integers `X` and `Y`
2. On the second line, read in a character name into a variable named `name`. For example _"Jozko Mrkvicka"_
3. Print text: _"`name` is located at coordinates `X`, `Y`"_, where `name`, `X`, and `Y` are variables from steps 1 and 2

_Note:_ Be careful about where the "cursor" remains after reading in variables `X` and `Y`