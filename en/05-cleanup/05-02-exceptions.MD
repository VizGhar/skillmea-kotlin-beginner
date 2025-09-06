# 5.2 Exceptions

Let's crash our own app now!

## 5.2.1 Block

Write a function `calculatePrice(quantity: Int, price: Double)`, which calculates the total price of products. Every third product should be free.

- `quantity` - number of products
- `price` - price of one product

Use `IllegalArgumentException` to throw an exception if inputs are invalid.

## 5.2.2 Order

Write a class representing an order. Let it have at least 2 attributes.
1. `status` - status of the order as a number
2. `id` - identifier of the order, for example `String`

The `status` will take one of the following values:
- `1` - created - allowed next states: 2 and 4
- `2` - processed - allowed next states: 3 and 4
- `3` - shipped - allowed next state: 4
- `4` - cancelled - allowed no further states

The class will also have a function to change the order status. If you call this function with an incorrect value, throw `IllegalStateException`.

## 5.2.3 Out Of Bounds

Write a function that takes in the height and width of a 2D surface as well as `X` and `Y` coordinates on that surface.
If the point `[X,Y]` is off the surface, either throw your own exception or find some suitable alternative.