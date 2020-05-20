---
layout: default
title: Installation
parent: Getting Started
nav_order: 1
---
# Installation
## Requirements

- **Operating System**
    - Mac OS, Linux and Windows 10
- **Compatible Python version**
    - Python 3.6, 3.7
- **Dependency**: 
    - shleeh (>=0.0.4)
    - nibabel (>=3.0.2)
    - SimpleITK ()>=1.2.4)
    - numpy (>=1.18.0)
    - pandas (>=1.0.0)
    - pillow (>=7.1.1)
    - tqdm (>=4.45.0)
    - openpyxl (>=3.0.3)
    - xlrd (>=1.0.0)

## Python build
- The installed Python must be compiled properly, 
If you use pyenv and are having any issue with python please refer following link: 
[Common Build Problems in PyENV](https://github.com/pyenv/pyenv/wiki/common-build-problems)
- To use gui feature, the installed python should compiled with tkinter module.
- You can test the tkinter installation with below command on your shell.

```js
$ python -m tkinter -c 'tkinter._test()'
```

- In Mac OSX, Homebrew installed tcl-tk and pyenv may have an issue with tkinter, please refer following link to solve the issue:
[Issue with Homebrew installed tcl-tk on pyenv](https://github.com/pyenv/pyenv/issues/1375)

## Install via PyPI
```js
$ pip install bruker==0.3.3rc0
```

## Install via Github
```js
$ pip install git+https://github.com/brkraw/bruker
```