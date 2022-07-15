---
title: Take Screenshot
description: Sub-Action to take a screenshot in OBS
published: true
date: 2022-07-15T18:32:12.923Z
tags: sub-action
editor: markdown
dateCreated: 2021-09-11T00:20:13.509Z
---

Up until now, you had to use OBS Raw to take a screenshot in OBS, here is a sub-action ot make things a bit simpler.

![sub-action-obs-takescreenshot-01.png](/sub-action-obs-takescreenshot-01.png)

`Scene`, `Source` and `File Path` all support variable replacements, and after a screenshot is successfully taken, the full file path is added back onto the arguments as `%screenshotFile%`.

There is a new date time friendly variable that can be used, `%filedatetime%` which is of the format `yyyyMMdd.hhmmss`.

## Variables

The following variables will be available after execution of this sub-action:

| Name | Description |
|-----:|:------------|
| `screenshotFile` | The full path to the screenshot that was taken
| `filedatetime` | Date Time varible that can be used for file name <br> `yyyyMMdd.hhmmss`
{.vars-table}