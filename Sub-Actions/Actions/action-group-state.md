---
title: Set Action Group State
description: Action Sub-Actions Reference
published: true
date: 2023-03-16T13:26:35.941Z
tags: 
editor: markdown
dateCreated: 2021-11-19T21:07:53.659Z
---

# Set Action Group State
Enables and Disables entire groups of actions 

`Group`	Defines which action group to affect
`State` What state should be set for each individual Action in that group. Valid options are `Enable`, `Disable` & `Toggle`

> For setting the state of individual actions see [Set Action State](/Sub-Actions/action-state)
{.is-info}

# Get Action Group State
## Variables

The following variables will be available after execution of this action:

Name | Description
----:|:------------
`actionGroupState` | Boolean for action group enabled state <br> `True / False`
`actionsEnabled` | A list of action IDs, of actions that are enabled
`actionsDisabled` | A list of action IDs, of commands that are disabled
{.vars-table}