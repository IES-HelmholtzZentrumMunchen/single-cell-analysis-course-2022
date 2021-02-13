---
title: Python programming
collapsible: false
---
To learn Python programming, there are several good online tutorials and courses. A good place to start is the [Python Beginner's guide](https://wiki.python.org/moin/BeginnersGuide) or the W3 [Python tutorial](https://www.w3schools.com/python/default.asp). In the following, I would like to nevertheless highlight a few features of the Python programming language. This is by no means a comprehensive list. If you know any Python tricks, or find some during the course, please do share them with everybody!

Before we go to code examples, a few Python features to keep in mind:
  * Variables are declared upon creation, this means you don't have to tell the Python interpreter what type of variable you declare. `x = 1` will be an integer, `x = "hello"` a string.
  * Variable names cannot start with a number, and cannot contain spaces, but underscores are fine, e.g. `channel_1 = np.array(...)`
  * Python is a very lightweight language. Almost all more advanced functionality needs to be imported from ***modules*** with the `import` statement. Upon import you can assign an alias for the module, very common is for example `import numpy as np`. Some modules have sub-modules that you can import on their own with `from ... import ...`, for instance `from matplotlib import pyplot as plt` imports pyplot, a very commonly used module for plotting.
  * Where most other programming languages (also 'R' that we use in the course for RNA-seq analysis) use `{` to begin loops or if/else statments and `}` to end them, Python uses indents (`Tab` key). Many programmers use tabs anyway to structure their code, and Python made this a requirement. If you get errors, check that you indented your code properly!
