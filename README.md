m154
================

<!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->

## Table of Contents

<!---
*.html linking works in browser, but not within the notebook
-->

1.  [Lecture 10 / Lab 2](lab2.html)
2.  [Homework 3](homework3.html)
3.  [Group Project](group_project.html)
    1.  [Getting started](#configuring-a-collaborative-workflow)

# Configuring a collaborative workflow

We’re going to be using Homebrew to install Miniconda, which is a
version of a python package manager called Anaconda. If you’re working
with the M1 Chip, then you have to download from source
[here](https://docs.conda.io/en/latest/miniconda.html).

Otherwise, you’ll need to install [Homebrew](https://brew.sh/). Then,
you’ll need to install
[Miniconda](https://formulae.brew.sh/cask/miniconda).

Then you’ll need to create an environment for this project. I named my
environment `m154env`.

``` shell
conda create -n <environment_name>
```

You can see the environment that you just created by running

``` shell
conda info --envs
```

You’ll want to activate the conda environment and install
[python](https://anaconda.org/conda-forge/python),
[jupyter](https://anaconda.org/conda-forge/jupyter),
[notebook](https://anaconda.org/conda-forge/notebook),
[rpy2](https://anaconda.org/conda-forge/rpy2), and any R-packages that
we’ll need
([r-randomforest](https://anaconda.org/conda-forge/r-randomforest),
[dplyr](https://anaconda.org/conda-forge/r-dplyr),
[tibble](https://anaconda.org/conda-forge/r-tibble)). The python,
jupyter, and notebook packages will allow us to select our conda
environment as a kernel for our jupyter notebook. The rpy2 package will
allow us to change the interpreter within a Python cell in our jupyter
notebook to instead interpret R code by entering `%%R` at the top of a
Python cell.

# Working locally

## Setting your environment variables

1.  Create a file named `.group_project_r_env` in the nbs folder
2.  In that file, define the following variables with the paths to each
    of the csv’s. I personally like to control-click on a file in Visual
    Studio Code, copy the entire path (represented by the `..` below),
    and then edit the last parts of the path to redirect it to what I’d
    like the path to point to, in this case that is the csv data.

``` shell
  GiveMeSomeCreditTrainingCSV=/../GiveMeSomeCredit/cs-training.csv
  GiveMeSomeCreditTestCSV=/../GiveMeSomeCredit/cs-test.csv
  GiveMeSomeCreditSampleEntryCSV=/../GiveMeSomeCredit/sampleEntry.csv
```

## How to Git

First, make sure that you have
[Git](https://formulae.brew.sh/formula/git) installed.

### Getting a copy of the repository onto your computer

I recommend using Visual Studio Code’s GitHub cloning functionality to
clone the respository. Otherwise, just run
`git clone https://github.com/TesfaAsmara/m154.git` in the folder where
you want the local repository to be stored.

### Saving your work

1.  `git status`
2.  `git add .`
3.  `git commit -m "some message about your work session goes here"`
4.  `git push`

### Getting ready to work

1.  Activate your environment `conda activate <environment_name>`
2.  `git status`
3.  `git pull`

You are now ready to work.

# Issues that came up

# Refreshing cache for gitignore

https://stackoverflow.com/questions/24410208/gitignore-does-not-ignore-folder
