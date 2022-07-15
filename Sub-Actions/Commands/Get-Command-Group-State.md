---
title: Get Command Group State
description: Commands Sub-Actions Reference
published: true
date: 2022-07-15T18:48:11.947Z
tags: subactions, commands
editor: markdown
dateCreated: 2022-07-15T18:48:11.947Z
---

##  Variables

The following variables will be available after execution of this sub-action:

| Name | Description |
|-----:|:------------|
| `commandGroupState` | Boolean for command group enabled state <br> `True / False`
| `commandsEnabled` | `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are enabled |
| `commandsDisabled` | `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are disabled |
{.vars-table}