---
title: Read Lines From File
description: File Sub-Actions Reference
published: true
date: 2022-12-04T19:11:42.532Z
tags: 
editor: markdown
dateCreated: 2021-10-24T23:49:24.324Z
---

## Overview
Using this sub-action, you can load the entire contents of a file into your action, each line will be added as a new variable, `%line#%` where `#` would be from 0 to n-number of lines in the file.

![sub-action-read-lines-from-file-001.png](/sub-action-read-lines-from-file-001.png)

## Configuration
### Parse Variables
If this option is selected, when reading in the lines, if there are any `%variables%` present, they will be parsed for you.

For example, you have a file of welcome messages, that consist of `Welcome %user%`, with variations on that, the `%user%` would be replaced when reading the file.

### Attempt Auto-typing
While reading the contents of the file, an attempt will be made on each line to auto-type it.  So if it's a number, it will make sure the variable contains a number type.