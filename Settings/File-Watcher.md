---
title: File Watcher
description: 
published: true
date: 2022-07-09T19:59:03.048Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:58.151Z
---

With the File Watcher option you can have an action react to:

The action specified will get the following variables:

Name | Description
----:|:------------
| `changeType` | The type of change, `Changed`, `Created`, `Deleted`
| `fullPath` | The full path to the file |
|`fileName` | The file name with extension |
| `name` | The file name without the extendion |
| `empty` | A boolean value indicating if the file is empty |

If you have `As JSON` ticked, it will add all root elements as arguments.

If `As JSON` is not ticked, it will add the following variables:

Name | Description
----:|:------------
| `lineCount` | The number of lines in the file |
| `line#` | The line of the file, replace # with the line number you want |
| `lineEscaped#` | The line of the file URL encoded, replace # with the line number you want |

### Sample screenshot

![image](/130543487-37f328d3-55b9-4dab-8f53-c46fde0ff967.png)