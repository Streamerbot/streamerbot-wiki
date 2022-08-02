---
title: Boolean
description: 
published: true
date: 2022-08-02T09:39:41.735Z
tags: 
editor: markdown
dateCreated: 2022-07-31T23:27:14.258Z
---

<font size="+3" class="mdi mdi-ab-testing primary--text"><b> Boolean</b></font>

---

## Overview

A Boolean is `true/false` (in C# lowercase and in native streamer.bot first letter uppercase)
A Boolean is **not** surrounded with anything
## Examples {.tabset}
### Example 1
```csharp
bool isTest = false
```
### Example 2
> the `{isTest}` is a Boolean but automatically gets turned to a string because of the `$""`
{.is-info}
```csharp
$"test status: {isTest}"
```

## If statements

In if statements you can do `if (variable)` and it checks if the variable it's true
So when you have the variable `isTest` and would do `if (isTest)` it would look if `isTest = true`

## Examples {.tabset}
### Example 1
```csharp
if (isTest)
{
// isTest `true`
}
else
{
// isTest `false`
}
```
### Example 2
```csharp
if (isTest)
{
CPH.SendMessage("true")
}
```

## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i> **Code *Go Back***](/en/Sub-Actions/Code)
{.btn-grid .mt-10}