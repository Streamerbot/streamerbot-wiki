---
title: Variable Types
description: A list of all available variable types that you can import in to your code
published: true
date: 2022-10-28T17:25:25.831Z
tags: 
editor: markdown
dateCreated: 2022-08-07T22:11:03.320Z
---

Below you see a list of importable variable types in C# code

## var
---

> `var` can be used if you don't know what variable type it is.
{.is-info}
```csharp
var variable = args["variable"];
```

## string
---
> `string` is for text not for numbers or other things.
{.is-info}
```csharp
string text = args["text"].ToString();
```

## int
---
> `int` is for **whole** numbers only.
{.is-info}
```csharp
int number = Convert.ToInt32(args["number"].ToString());

```

## bool
---
> `bool` is for `true` `/` `false`
{.is-info}
```csharp
bool boolean = Convert.ToBoolean(args["boolean"]);
```

## float
---
> `float` is for numbers with up to 7 decimals after the comma
{.is-info}
```csharp
float sevenDecimal = float.Parse(args["sevenDecimal"].ToString());
```

## double
---
> `double` is for numbers with up to 14 decimals after the comma
{.is-info}
```csharp
double fourteenDecimal = Convert.ToDouble(args["fourteenDecimal"]);
```

## decimal
---
> `decimal` is for numbers with up to 28 decimals after the comma
{.is-info}
```csharp
decimal twentyEightDecimal = Convert.ToDecimal(args["twentyEightDecimal"]);
```

## all
```csharp
var variable = args["variable"];
string text = args["text"].ToString();
int number = Convert.ToInt32(args["number"].ToString());
bool boolean = Convert.ToBoolean(args["boolean"]);
float sevenDecimal = float.Parse(args["sevenDecimal"].ToString());
double fourteenDecimal = Convert.ToDouble(args["fourteenDecimal"]);
decimal twentyEightDecimal = Convert.ToDecimal(args["twentyEightDecimal"]);
```

---

- [<i class="mdi mdi-chevron-left"></i> **Code *Go Back***](/en/Sub-Actions/Code)
{.btn-grid .my-5}