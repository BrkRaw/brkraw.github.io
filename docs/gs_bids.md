---
layout: default
title: BIDS converter
parent: Getting Started
nav_order: 3
---

# BIDS converter
![brkraw bids](../imgs/brkraw_bids.png)
**The usage of the command-line tool 'brkraw' for BIDS data organization.**

- Upgraded feature to reduce the burden on renaming and organizing according to BIDS guideline.
- The fully organized data can be generated by creating and fill out a BIDS datasheet 
(MS Excel format) from the large set of raw Bruker data. Simply put all raw Bruker data (or zipped) into a folder and
run 'brkraw bids_helper' command with *\<input dir\>* and your preferred *\<output filename\>*.
- The JSON syntax template allows building a JSON metadata to meet the BIDS requirement for each converted image. The 
module provides this JSON syntax template according to BIDS v1.2.2 in case of adding the option '-j' on the command.
- The bids_convert command also will generate empty template of `dataset_description.json` and `README` to better fit
with BIDS guideline, please make sure test your data with official 
[BIDS validator](https://bids-standard.github.io/bids-validator/)

- Below command shows how to generate BIDS datasheet with JSON syntax template

```js
$ brkraw bids_helper <input dir> <output filename> -j
```

- Update the datasheet.xlsx. In some cases, it is necessary to update the datasheet.xlsx. There are multiple columns without 
pre-filled value in the datasheet.xlsx file. Here is a little explaination:  

  | Column Name | Purpose | Valid value | If omitted |
  | --- | --- | --- | --- |
  | task  | form the `_task-<label>` part of output filename for the scan | value compitable with BIDS | omitted in output file name, invalid for func |
  | acq  | form the `_acq-<label>` part of output filename for the scan | value compitable with BIDS | omitted in output file name |
  | ce  | form the `_ce-<label>` part of output filename for the scan | value compitable with BIDS | omitted in output file name |
  | rec  | form the `_rec-<label>` part of output filename for the scan | value compitable with BIDS | omitted in output file name |
  | dir  | form the `_dir-<label>` part of output filename for the scan | value compitable with BIDS | omitted in output file name |
  | modality  | form the `_<modality>` part of output filename for the scan | value compitable with BIDS | use guessed value from method, maybe invalid in some cases |  
  
  For example, if you have a “Gradient echo EPI” scan for BOLD purpose, you could fill in datasheet.xlsx 
  with "bold" under "modality" column and "resting" under "task" column for the corresponding scan.
  If you don't put "bold" as modality, it may generated a file with name containing "EPI", fails the bids validator. 

- After updating the datasheet and syntax, the below command will generate a fully organized BIDS dataset 
to *\<output dir\>* with JSON header files for each converted image by parsing the parameters specified on 
*\<JSON syntax template.json\>*.

```js
$ brkraw bids_convert <input dir> <BIDS datasheet.xlsx> -j <JSON syntax template.json> -o <output dir>
```

- To learn more detail about building your own JSON syntax template, please check our example in
[Jupyter Notebooks](https://mybinder.org/v2/gh/BrkRaw/tutorials/ac95b2c87b05664cb678c5dc1a930641397130ed)