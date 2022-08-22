---
title: Take Screenshot
description: Sub-Action to take a screenshot in OBS
published: true
date: 2022-07-15T18:35:47.141Z
tags: sub-action, obs-studio
editor: markdown
dateCreated: 2021-09-11T00:20:13.509Z
---

## Overview

Take a screenshot in [OBS Studio](/en/Broadcasters/OBS)

![sub-action-obs-takescreenshot-01.png](/sub-action-obs-takescreenshot-01.png)

## Configuration
### Connection
Select the target OBS Studio instance

### Scene
Select the scene to screenshot

This input accepts [variables](/en/Variables)

### Source
Select the source to screenshot

This input accepts [variables](/en/Variables)


### Filepath
Select the file path to save the resulting `.png` file

This input accepts [variables](/en/Variables)

### Quality
Select the desired image quality or leave as `Auto`


## Variables

The following variables will be available after execution of this sub-action:

| Name | Description |
|-----:|:------------|
| `screenshotFile` | The full path to the screenshot that was taken
| `filedatetime` | Date Time varible that can be used for file name <br> `yyyyMMdd.hhmmss`
{.vars-table}