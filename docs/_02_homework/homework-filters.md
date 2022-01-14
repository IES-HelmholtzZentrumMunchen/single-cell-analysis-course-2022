---
title: Build an image processing pipeline to detect cells
date: 2021-02-23 15:00:00CET
---
In this homework, you will apply image filters and thresholding to identify cells in images. We have an annotated data set prepared that will allow you to test the quality of your image processing pipeline against manually annotated cells. After preparing a function for processing, you should process all images to find out how well your pipeline works over a greater data set.

General steps of the image processing pipeline:
  * Read the images
  * Remove noise by an appropriate filter
  * Threshold the image
  * Apply appropriate morphological filters
  * Compare the outcome to the manually annotated image
  * Save the result
