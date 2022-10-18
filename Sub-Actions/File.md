---
title: File Operations
description: Reading and Writing files with sub-actions
published: true
date: 2022-10-18T06:47:13.452Z
tags: 
editor: markdown
dateCreated: 2022-01-23T19:39:55.125Z
---

Streamer.bot has the capability of reading the contents of files into variables and writing back to files when needed.

* [<i class="mdi mdi-file-find primary--text"></i>**Read Lines From File *Load the entire contents of a file into your action***](/en/Sub-Actions/File/Read-Lines-From-File)
* [<i class="mdi mdi-file-move primary--text"></i>**Read Random Line From File *Read random line from a file***](/en/Sub-Actions/File/Read-Random-Line-From-File)
{.btn-grid .my-5}

---

## Write to File

Using this sub-action, it allows you to write data from a variable to a file, which can then be used for other things later if you so choose. So, any of the variables listed you can extract the data from and write to this file.


![write_to_file.png](/write_to_file.png)

### Append to file 
Appending to a file will add the incoming data to the end of the file. So, the data when it changes in the %userName% variable will be ‘appended’ to the end of the file. It does not overwrite the existing data. 

If the Append to File option is unchecked it will overwrite everytime each time new data is written.

---
  
- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/en/Sub-Actions)
- [<i class="mdi mdi-state-machine primary--text"></i> **Logic *Sub-actions reference for custom logic operations***](/en/Sub-Actions/Logic)
{.btn-grid .my-5}