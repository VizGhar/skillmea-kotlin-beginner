# 7.4 Open Attributes and Functions

So far we've had quite some tied hands. The only option we had when it came to inheritance was basically copying and pasting the entire management of some class. With open attributes and functions (or members), we can now modify these "copy-paste" things.

## 7.4.1 Shapes

1. Create a `Shape2D` class without attributes
2. In the `Shape2D` class, create a function `perimeter` (circumference) that returns a `Double`
3. In the `Shape2D` class, create a function `area` (content) that returns a `Double`
4. Create a `Circle` class that extends `Shape2D`
5. Properly implement functions `perimeter` and `area` in the `Circle` class
6. Similarly, create and implement `Rectangle`

## 7.4.2 Codes

1. Create a `Cipher` class without attributes
2. In the `Cipher` class, create a function `encode(text)`, which returns an encoded text
3. In the `Cipher` class, create a function `decode(text)`, which returns a decoded text
4. Implement and extend `SubstitutionCypher`, a substitution cipher, that extends `Cipher`
5. Implement and extend `ShiftCypher`, a shift cipher, that extends `Cipher`

Design the details of these classes yourself.