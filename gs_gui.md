---
layout: default
title: Graphic User Interface (GUI)
parent: Getting Started
nav_order: 4
---
# Graphical User Interface (GUI)

- Run GUI with input and output path
```js
$ brkraw gui -i <session path> -o <output path>
```

![brkraw GUI](../imgs/brkraw_gui.png)
**brkraw gui interface.**

- You can run GUI without any path option. It will show you only two buttons (Open File / Open Directory). 
If you are opening zipped PVdataset, please use the 'Open File' button. In other cases make sure you are in the 
PVdataset root folder where the subject file is located. If you do not enter into the dataset folder, the GUI 
will freeze. In this case, you will need to force quit the GUI.

```js
$ brkraw gui
```
