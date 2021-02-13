---
title: Numpy arrays
collapsible: true
---
Because numpy arrays are essential for image processing, let's take a closer look at them. All of the below examples require numpy to be imported
```python
import numpy as np
```
You can generate an array in multiple ways:
```python
x = np.array([1,2,3,4,5,42])
print(x)
array([ 1,  2,  3,  4,  5, 42])
```
This is a one-dimensoinal array. Check it's dimensions and number of elements like this:
```python
x = np.array([1,2,3,4,5,42])
x.ndim
1
x.shape
(6,)
```
The method `ndim` outputs the array dimension and `shape` returns the number of elements along each dimension, in this case we have 1 dimension and 6 elements.
Let's construct a 2-dimensional array:
```python
x = np.array([[1,2,3],[5,6,7]])
x.ndim
2
x.shape
(2,3)
```
Arrays are a very important concept in image analysis, so take some time to understand how they are built.
