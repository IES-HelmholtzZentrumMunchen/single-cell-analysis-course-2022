---
title: General coding concepts
collapsible: true
---
In this course, we will with only handful of Python functions, but you can already do ***a lot*** with those.
But before we start, let's have a general view on programming concepts. Feel free to skip this if these are already familiar to you.

#### Comments
These are part of your code that is not executed. Very useful to make notes and very important even for seasoned programmers to understand what your code is doing. In Python, a comment starts with `# a comment` and extends to the end of the line. If you need multi-line comments, you can use triple quotation marks `""" my very long comment """`.

#### Variables

Variables are a holder for anything, for example a single number, a text, or a whole image. They can also point to functions or classes. In most programming languages, variables are assigned like this:
```python
x = 42
```
However, in some programming languages, you have to ***declare*** the type of your variable, meaning that you have to say which data type they will hold. Compare the above (Python) declaration to one in Java.
```java
int x = 42;
```
Note that you have to tell the java compiler not only that you declare a number, but that this is will be integer. (Also note that in Java you have to end every line with a `;`.)
In 'R', you can use `=` or the `->` operator.
```r
x = 42
x <- 42
42 -> x
```
Variables can come in different types. The Python interpreter takes care to recognize automatically what kind of variable you want to declare.
```python
x = 42 # an integer
x = [1,2,3,4,5,42] # a list
x = "hello" # a string
x = "42" # also a string
x = np.array([1,2,3,4,5,42]) # a numpy array
```
There are even more specialized types of variables, like dictionaries, data frames, etc. which we will discuss when we need them.

#### Indexing

Let's have a closer look at lists and arrays, They hold multiple values. Each value can be accessed by an index.
```python
x[0]
1
x[6]
42
```
Note that in Python, indexing starts at `0`. In 'R', indexing always starts at `1`.
```r
x <- c(1,2,3,4,5,42)
x[1]
1
x[0]
numeric(0) # no sensible output
```
In Python, also text is indexed.
```python
x = "hello"
x[1]
'e'
```
An interesting variant of indexing is 'boolean indexing'. Here you create on-the-fly a condition that is then used to get the values you want.
```r
x = c(1,2,3,4,5,42)
x[x>4]
5 42
```
In this example, you 'select elements of x, where x is greater than 4'. Where is the boolean part of it all? Just type
```r
x = c(1,2,3,4,5,42)
x>4
FALSE FALSE FALSE FALSE  TRUE  TRUE
```
Now you can see the boolean array that is generated and used as index to obtain all elements that evaluate to `TRUE`.

#### Operators

Operators are used to assign, modify, or compare variables. Have a look at the [operators in Python](https://www.w3schools.com/python/python_operators.asp).
Most operators should be self-explanatory, but let's have a closer look at comparison, logical, and identity operators. The first ones are used to compare values.
```r
x = 42
y = 43
x == y
FALSE
```
So, depending on the outcome of the comparison, you get `TRUE` or `FALSE`. This can be used in logical comparisons. Here the logical operator `and` evaluates to `true` only if both sides are `true`.
```python
x = 42
y = 43
z = 100
y > x
True
y > x and y < z
True
```
An extension of the logical operators are 'membership operators'. You can  check if one value is part of a Python list with `in` or, say, a vector if you are using 'R' by using `%in%`.
```r
x = c(1,2,3,4,5,42)
43 %in% x
FALSE
42 %in% x
TRUE
```

#### Loops

#### If / else statements

#### Functions

Often you will want to use functions if you use the same code repeatedly. As a rule of thumb, if you use a part of your code more than once, consider writing a function. Functions also help to structure your code and make it more reusable.
A function typically gets a name assigned and we can define what kind of variables and parameters go into the function.
```python
def my_add(x,y):
  return(x + y)
my_add(1,2)
3
```
