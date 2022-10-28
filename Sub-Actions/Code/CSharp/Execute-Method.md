---
title: Execute C# Method
description: 
published: true
date: 2022-08-02T09:40:30.435Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:54.418Z
---

## Execute C# Method
Using this sub-action, you can call into an existing execute code, and call another method, or it's main entry point.  If you have the Execute C# Code setup for `Keep Alive` and `Precompile on Startup` you can use `private` variables within the class to preserver data between calls.

The methods must be in the form of, a return type of `bool` with no parameters:

```csharp
public bool MethodName()
{
    // your code here
    return true;
}
```
The capabilities of this sub-action maybe extended later.

---

- [<i class="mdi mdi-chevron-left"></i> **Code *Go Back***](/en/Sub-Actions/Code)
{.btn-grid .my-5}