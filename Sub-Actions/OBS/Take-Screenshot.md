---
title: Take Screenshot
description: OBS Studio Sub-Action Reference
published: true
date: 2023-03-16T11:41:07.120Z
tags: sub-action, obs-studio
editor: markdown
dateCreated: 2021-09-11T00:20:13.509Z
---

## Overview
Makes a screenshot from a `scene` or `source`

![overview.png](/Sub-Actions/OBS/take-screenshot/overview.png =400x)

## Configuration
### Scene
The scene, this can use variable like `%currentScene%`

### Source
The source, can be empty

### Filepath
Select the file path to save the resulting file like `.png` or `.jpg`

### Quality
Select the desired image quality or leave as `Auto`

## Variables
Name | Description
----:|:------------
`screenshotFile` | The full path to the screenshot that was taken
`filedatetime` | Date Time variable that can be used for file name <br> `yyyyMMdd.hhmmss`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio Sub-Actions *Go Back***](/Sub-Actions/OBS)
{.btn-grid .my-5}