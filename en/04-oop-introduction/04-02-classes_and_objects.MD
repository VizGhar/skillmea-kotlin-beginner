# 4.2 Classes and Objects

Now you know how to create a class and objects from it. Classes and objects are always in the relationship of `1-n`. That means one class can have `0` and more instances called objects.

## 4.2.1 Position

This is one of the most classic classes, which we understand the basics.
Create a class named `Position`, which will have attributes `x` and `y`.

In the `main` function create 3 instances of this class and set them to different values. Then print these values on standard output.

## 4.2.2 Address

If your application works with databases, you often describe users of applications. One of such information is also an address. If you would keep it in one text field, you easily run into limits when filtering or sorting items.

So create a class `Address` representing a physical address. Create two instances. One represents you, the other your friend. Write a function for pretty printing an address.

## 4.2.3 Inception

Write a class `User` with the following fields:
1. `username: String`
2. `email: String`
3. `pass: String`
4. `address: Address`

Now you see that one object can contain another object.