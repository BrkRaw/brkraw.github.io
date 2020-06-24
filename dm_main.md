---
layout: default
title: Data management
nav_order: 3
has_children: false
---

# Data management tool
![brk-backup](../imgs/brk_backup.png)
**brk-backup script utilizing the Python API to immediately access both raw data and archived data 
to parse the metadata for data management.**

- Print out archived dataset and its condition
```js
$ brk-backup archived <rawdata path> <backup path> [-l]
```

- Print out review backup status
```js
$ brk-backup review <rawdata path> <backup path> [-l]
```

- Archive data from rawdata path to backup path, if the dataset has been archived and identical, then skip
```js
$ brk-backup backup <rawdata path> <backup path>
```

- Remove files classified as unnecessary via review process among backed up data. The interactive UI will ask you
to confirm each step to prevent erase important data
```js
$ brk-backup clean <rawdata path> <backup path>
```