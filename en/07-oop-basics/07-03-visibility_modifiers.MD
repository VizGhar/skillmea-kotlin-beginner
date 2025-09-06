# 7.3 Access Modifiers

We don't want everything from our old times to be visible in our inherited class.
To achieve this, we'll use access modifiers.

## 7.3.1 Substitution Cypher - Private Attribute

Write a class for encoding and decoding a substitution cipher.
The key will always be a text that contains all letters `a-z` in random order.

For example, if the key is `_xyzabcdefghijklmnopqrstuvw_`, the letter `A` will be mapped to `X`,
the letter `B` to `Y`, and so on (see entire mapping below)

```
xyzabcdefghijklmnopqrstuvw
abcdefghijklmnopqrstuvwxyz
```

1. Create a class `SubstitutionCypher` with a private attribute `key`
2. Implement an encode function that uses the secret key
3. Implement a decode function that uses the secret key

Do you think it would be suitable to keep this `key` as a public attribute?

## 7.3.2 Level - Private Function

Create a class that holds a 2D map of your game `map` and a character's position `x` and `y`.
Create in it functions:

1. `look(direction: Int): Char?`, which determines what object is located in the direction `direction` from your character
2. `go(direction: Int): Unit`, which tries to move the character in the direction `direction`

The direction can have values 0-3 representing directions `LEFT`, `TOP`, `RIGHT`, `BOTTOM`

Both of these functions may want to control whether you accidentally get an object out of bounds.
I recommend setting up a private function to check boundaries - `inBounds(x: Int, y: Int): Boolean`

## 7.3.3 File Private

Repeat task 7.3.1, but do not create a class. Instead, create a new file with public functions
`encode` and `decode`. The `key` is hardcoded in this file and, of course, private.