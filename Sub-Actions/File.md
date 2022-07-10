---
title: File Operations
description: Reading and Writing files with sub-actions
published: true
date: 2022-07-10T18:56:47.197Z
tags: 
editor: markdown
dateCreated: 2022-01-23T19:39:55.125Z
---

Streamer.bot has the capability of reading the contents of files into variables and writing back to files when needed.

## Read Lines From File

Using this sub-action, you can load the entire contents of a file into your action, each line will be added as a new variable, `%line#%` where `#` would be from 0 to n-number of lines in the file.

![sub-action-read-lines-from-file-001.png](/sub-action-read-lines-from-file-001.png)

### Parse Variables
If this option is selected, when reading in the lines, if there are any `%variables%` present, they will be parsed for you.

For example, you have a file of welcome messages, that consist of `Welcome %user%`, with variations on that, the `%user%` would be replaced when reading the file.

### Attempt Auto-typing
While reading the contents of the file, an attempt will be made on each line to auto-type it.  So if it's a number, it will make sure the variable contains a number type.

---

## Read Random Line From File

Using this sub-action, you can load the entire contents of a file into your action, then you can have the bot read a random line from the file and load it into a variable `%randomLine%`.

![sub-action-readrandomlinefromfile-01.png](/sub-action-readrandomlinefromfile-01.png)

### Parse Variables
If this option is selected, when reading in the lines, if there are any %variables% present, they will be replaced with the current contents of the specified variable. 
Example:

You have a file containing a list of welcome messages, such as: 
    Welcome `%user%`.
  Greetings `%user%`.
  Nice to see you `%user%`, have a seat.

The `%user%` would be replaced when reading the file.

### Attempt Auto-typing
While reading the contents of the file, an attempt will be made on each line to determine its ‘type’. So, if it's a number, it will make sure the variable is defined as a numeric, if it contains a string it will define the variable as a string. This is useful for future operations on the created variable.

---

## Write to File

Using this sub-action, it allows you to write data from a variable to a file, which can then be used for other things later if you so choose. So, any of the variables listed you can extract the data from and write to this file.


![write_to_file.png](/write_to_file.png)

### Append to file 
Appending to a file will add the incoming data to the end of the file. So, the data when it changes in the %userName% variable will be ‘appended’ to the end of the file. It does not overwrite the existing data. 

If the Append to File option is unchecked it will overwrite everytime each time new data is written.

