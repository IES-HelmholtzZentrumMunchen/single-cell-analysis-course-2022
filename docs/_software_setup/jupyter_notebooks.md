---
title: Jupyter notebooks
---
For the image analysis part of this course, we will make use of [Jupyter notebooks](https://jupyter.org/). Jupyter notebooks and iPython on which Jupyter is based, have been ranked by *Nature* as one of the [top ten computer codes that transformed science](https://www.nature.com/articles/d41586-021-00075-2). You will quickly appreciate the power of Jupyter which allows you to run Python code **interactively** so you can right away explore the outcome of your processing step or analysis, and thus makes prototyping analysis pipelines fast (and fun!). In addition you can write nicely formatted comments by using [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

To start Jupyter, start the conda command line prompt and activate the environment you just created.
```
(base):$ conda activate scater
```
Start a new jupyter notebook like this:
```
(scater):$ jupyter notebook
```
This should open a browser where you can make a new notebook file. To work with Jupyter notebooks effectively, check out the [Datacamp Jupyter cheat sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Jupyter_Notebook_Cheat_Sheet.pdf).

We recommend to memorize a few hot keys that will make working with Jupyter notebooks way faster and more fun. When you click on a cell, you are in the 'Edit' mode. You can leave the 'Edit' mode by pressing the `Esc` key. Now you are in command mode in which you can create or erase cells. Most often you may want to:
  * Create a new cell: Press `Esc` then  `A` , to create a new cell above, or
  * Press `Esc`, then `B` to create a new cell below.
  * Press `Esc`, then `X` to erase a cell.
  * In edit mode press `Ctrl + Enter` to run the current cell.
  * Press `Shift + Enter` to run the current cell and make a new one below.

If you want to write a comment, change the type of cell to 'Markdown' in the dropdown menu. Once run, your cell will convert to a nicely formatted text. You can even add formulas following the [LaTeX](https://www.latex-project.org/) language.
