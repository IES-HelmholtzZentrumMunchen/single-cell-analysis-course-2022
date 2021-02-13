---
title: Loops and list comprehension
collapsible: true
---
As mentioned, loops in python are defined by indents. Have a look at the following:
```python
for x in range(3):
  for y in range(2):
    print("x is {} and y is {}".format(x,y))

x is 0 and y is 0
x is 0 and y is 1
x is 1 and y is 0
x is 1 and y is 1
x is 2 and y is 0
x is 2 and y is 1
```
Note that `range` generates values starting from 0. Each block of code within the loop needs to be indented one additional time to be executed properly.
An exception to the tabulation approach are 'list comprehensions'. This is a very 'pythonic' approach to pack the output of a loop in one go into a list. This may be confusing at first, but try to understand the following example:
```python
my_list = [x*y for x in range(3)  for y in range(2)]

print(my_list)
[0, 0, 0, 1, 0, 2]
```
Compare it to the output of the loop above. During each execution, x is multiplied with y and the resulting value is written into the list. Alternatively, you could use regular loops to achieve the same result by appending the result using `list.append()` like so:
```python
my_list = []
for x in range(3):
  for y in range(2):
    my_list.append(x*y)

print(my_list)
[0, 0, 0, 1, 0, 2]
```
But this is much more verbose than a list comprehension, isn't it?
