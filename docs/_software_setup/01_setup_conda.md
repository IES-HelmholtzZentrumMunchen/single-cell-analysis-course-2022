---
title: How to set up a python environment
---
We highly recommend using anaconda as Python packet manager. There are other ways to install Python but you will be on your own. In any case, we recommend using a packet manager and working with Python environments. You can think of environments as independent installations that contain their own set of modules. Using environments for different tasks makes sure that you won't run into conflicts, which may emerge if for example one software module is not maintained any more.

First, please install Anaconda or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) for you operating system. Miniconda only has the minimal number of modules pre-installed and will be sufficient for this course.

After conda is installed, open the conda command line. Follow the next steps to create a new environment and install Python and the required Python modules. You can either install the required modules manually:
```
(base):$ conda create -n scater
(base):$ conda activate scater
(scater):$ conda install python
(scater):$ conda install scikit-image
(scater):$ conda install scipy
(scater):$ conda install pandas
(scater):$ conda install tensorflow
(scater):$ conda install jupyter
(scater):$ pip install stardist
```
OR use the provided yml file:
```
(base):$ conda env create -f scater.yml
(base):$ conda activate scater
```
