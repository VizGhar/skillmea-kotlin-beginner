# 4.4 Instance Functions

Besides data transfer, objects can also have some behavior. We will explore this on the following exercises.

## 4.4.1 Time

Write a class `Time` representing time in hours and minutes with the following methods:

1. `addMinutes(m: Int)`: returns a new time shifted by `m` minutes ahead (properly wraps around 60 min)
2. `toString()`: returns the time in format `HH:MM`, e.g. "09:05"
3. `isBefore(other: Time)`: determines if the current time is before another time
4. `totalMinutes()`: returns the number of minutes from midnight
5. `diff(other: Time)`: returns the difference between times in minutes (as an integer)

## 4.4.2 Fractions

Write a class representing a fraction. It has a numerator and a denominator.

Write methods for:
1. adding fractions
2. subtracting fractions
3. converting a fraction to its simplest form
4. adding an integer to a fraction
5. subtracting an integer from a fraction

These operations should always return a new fraction instance (numerator and denominator must be `val`)