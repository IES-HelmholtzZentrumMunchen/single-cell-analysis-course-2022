---
title: General coding concepts
collapsible: true
---
In this course, we will work with only a handful of Python functions, but you can already do ***a lot*** with those.
But before we start, let's have a general view on programming concepts. Feel free to skip this part if these concepts are already familiar to you.

#### Comments
These are part of your code that is not executed. It is very useful to make notes and very important, even for seasoned programmers, to understand what your code is doing. In Python, a comments look like this: `# a comment`. The comment starts with `#` and extends to the end of the line. If you need multi-line comments, you can do it like this `""" my very long comment """`. Everything between the triple quotation marks `"""` will be interpreted as a comment.

#### Variables

Variables are a placeholder for any data. This can be for example a single number, a text, or a whole image. They can also point to functions or classes. In most programming languages, variables are assigned like this:
```python
x = 42
```
However, in some programming languages, you have to ***declare*** the type of your variable, meaning that you have to say explicitly which data type they will hold. Compare the above (Python) declaration to one in Java.
```java
int x = 42;
```
Note that you have to tell the java compiler not only that you declare a number, but that this will be integer. (Also note that in Java you have to end every line with a `;`.)
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
There are even more specialized types of variables, like dictionaries, data frames, etc. which we will introduce and discuss during the course when we need them.

#### Indexing

Let's have a closer look at lists and arrays. They hold multiple values. Each value can be accessed by an index.
```python
x = [1,2,3,4,5,42]
x[0]
1
x[6]
42
```
Note that in Python indexing starts at `0`. In 'R', indexing always starts at `1`.
```r
x <- c(1,2,3,4,5,42)
x[1]
1
x[0]
numeric(0) # no sensible output
```
In Python, also strings are accessible by index.
```python
x = "hello"
x[1]
'e'
```
An interesting variant of indexing is 'boolean indexing'. Here you create on-the-fly a condition that is then evaluated to return the values you want.
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
Make sure you understand the effect of logical operations. Note that in this example, `True` and `False` are boolean values, not names of variables.
```python
True and True
True
True or False
True
False or False
False
False and False
False
```
An extension of the logical operators are 'membership operators'. You can check if one value is part of a Python list with `in` or, if you are using 'R' with `%in%`, respectively.
```r
x = c(1,2,3,4,5,42)
43 %in% x
FALSE
42 %in% x
TRUE
```

#### Loops
Loops make a part of code execute until a condition is met, or all elements of a list or array are processed. You can construct loops in most programming languages with `while` or `for`. Try to understand the differences between both approaches.
```python
x = [1,2,3,4,5,42]
for i in range(len(x)):
  print(x[i])
1
2
3
4
5
42

i=0
while i<len(x):
  print(x[i])
  i=i+1
1
2
3
4
5
42
```
Understand what is happening. In the first case, we first see how many items we have in `x` by using `len(x)`. Then we use the python method `range` to construct a sequence of numbers from `0` to `len(x)`. Then we use this sequentially increasing number as index to access an element in the list `x` and print it. In the `while` loop, we have to first initialize our counter `i`, then set a condition until when the loop should run. Be sure to increase your counter at the end of the loop so that you condition will be met, otherwise your loop will not stop to run and you will have to force quit your Python interpreter.

#### If / else statements

Very frequently, you will want to execute a function or other code only when a specific condition is met. Most programming languages use some kind of `if...else` syntax for this.
```r
x = 42
if(x >= 42){
  print("The meaning of life.")
}
"The meaning of life."

x = 42
if(x > 42){
  print("The meaning of life.")
}
# no output
```
Use if/else statements if you have alternatives to choose from.
```
if condition == True:
  # analyze data
else:
  # do nothing
```

#### Functions

Often you will want to use functions if you use the same code repeatedly. As a rule of thumb, if you use a part of your code more than once, consider writing a function. Functions also help to structure your code and make it more reusable.
A function typically gets a name assigned and we can define what kind of variables and parameters go into the function.
```python
def my_add(x,y):
  return(x + y)
my_add(1,2)
3
```
