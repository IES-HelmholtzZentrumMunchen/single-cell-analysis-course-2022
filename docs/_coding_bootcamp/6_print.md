---
title: Print
collapsible: true
---
*"Debugging with print is like washing your dishes with your fingers: Highly underrated and highly effective."*
I rarely follow Twitter wisdom but that one struck a bell with me. If you want to know what your function is doing, it really helps me to print out variables, meaning to display them as text.
```python
x = 42
print(x)
42
```
But you can do more things with `print`. Since Python 3, you can format variables and combine them with text to generate output elegantly:
```python
x = 42
print("The meaning of life is {}.".format(x))
"The meaning of life is 42."
```
