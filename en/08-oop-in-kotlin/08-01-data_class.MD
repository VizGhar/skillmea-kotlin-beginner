# 8.1 Data Classes

Data classes are classic classes with implemented functions `hashCode`, `toString`, and `equals`.

## 8.1.1 Parser

From the provided text file ([00-attachments/samples.txt](../00-attachments/samples.txt)) read all lines, where the user identifier is name, surname, and age. Thus, two lines with the same name, surname, and age are _duplicate_ regardless of email and color.

How many lines would be left in this document if we removed these duplicate lines?

Task: Try to solve it without and with data classes.

<details>

<summary>Helpful list of duplicate records</summary>

Triplets `name` `surname` `age`, which have AT LEAST 2 occurrences:

```
DAVID, FLORES, 20
NICHOLAS, BRYANT, 25
HOWARD, TAYLOR, 24
...
```