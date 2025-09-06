# 3.4 Named arguments

Your function header should look like this:
```kt
fun createWelcomeMessage(
    name: String,
    greeting: String = "Ahoj",
    punctuation: String = "!)",
    uppercase: Boolean = false,
    emoji: String = ""
): String
```

The output of this function will be for example:
> AHOJ JANKO! 👋

Try using this function

## 3.4.1 ASCII Frame

Write your own function to print the text in a frame. If the input text is _"Hello"_ and the other default values, it should look like this:

```
#########
#       #
# Hello #
#       #
#########
```

You can modify:
1. the frame height (default `1`)
2. the internal padding (default `1`)
3. the character representing the frame (default `#`)