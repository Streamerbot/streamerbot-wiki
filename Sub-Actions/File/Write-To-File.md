---
title: Write To File
description: 
published: true
date: 2022-10-18T06:54:28.030Z
tags: write to file
editor: markdown
dateCreated: 2021-11-20T01:38:58.905Z
---

## Overview
Using this sub-action, it allows you to write data from a variable to a file, which can then be used for other things later if you so choose. So, any of the variables listed you can extract the data from and write to this file.

![write_to_file.png](/write_to_file.png)

## Configuration
### Append to file 
Appending to a file will add the incoming data to the end of the file. So, the data when it changes in the %userName% variable will be ‘appended’ to the end of the file. It does not overwrite the existing data. 

If the Append to File option is unchecked it will overwrite everytime each time new data is written.

You can capture more that one variable at anytime.