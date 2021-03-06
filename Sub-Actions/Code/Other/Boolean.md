---
title: Boolean
description: 
published: true
date: 2022-07-31T23:27:14.258Z
tags: 
editor: markdown
dateCreated: 2022-07-31T23:27:14.258Z
---

<h1 class="mdi mdi-ab-testing primary--text"> Boolean</h1>

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