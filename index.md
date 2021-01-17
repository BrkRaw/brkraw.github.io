---
layout: default
title: Home
nav_order: 1
description: "Compregensive tool to access raw Bruker Biospin data"
permalink: /
---

[![DOI](https://zenodo.org/badge/245546149.svg)](https://zenodo.org/badge/latestdoi/245546149)

# BrkRaw: A comprehensive tool to access raw Bruker Biospin data
#### Version: 0.3.3

## Introduction

The 'BrkRaw' is a python module providing flexibility in handling data with advanced functionalities that 
the conventional converter did not provide, which includes

1. Python API to load data with image analysis friendly image object ([nibabel](https://nipy.org/nibabel/) or 
[simpleITK](https://simpleitk.readthedocs.io/en/master/gettingStarted.html#python-binary-files)).
2. The fidelity of correct orientation and coordinates based on the subject and scanner space.
3. Excel sheet guided automate [BIDS](https://bids.neuroimaging.io) organizer.
4. Command-line tools to help quickly access data before conversion (check data information and GUI previewer)
    
### Statement of need
We designed this python module aims for the preclinical MRI researcher or MR physician who utilizing the Bruker 
preclinical MRI scanner for their research as well as medical imaging scientists who interested in accessing 
preclinical MRI data more flexible manner.

### Getting start
1. [Installation](https://brkraw.github.io/docs/gs_inst.html)
2. [How to convert assess and convert raw data into NifTi format](https://brkraw.github.io/docs/gs_nii.html)
3. [How to convert and organize into BIDS of the multiple data](https://brkraw.github.io/docs/gs_bids.html)
4. [How to preview data without conversion](https://brkraw.github.io/docs/gs_gui.html)

### Tutorials
1. [Python API - Jupyter notebook](https://mybinder.org/v2/gh/BrkRaw/tutorials/ac95b2c87b05664cb678c5dc1a930641397130ed)