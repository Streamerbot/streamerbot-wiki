---
title: Import Variables
description: 
published: true
date: 2022-07-09T03:24:07.859Z
tags: 
editor: markdown
dateCreated: 2022-06-27T03:40:03.549Z
---

# Import Variables
## var
---

> `var`can be used if you don't know what variable type it is.
{.is-info}
```csharp
var variable = args["variable"];
```

## string
---
> `string`is for text not for numbers or other things.
{.is-info}
```csharp
string text = args["text"].ToString();
```

## int
---
> `int`is for **whole** numbers only.
{.is-info}
```csharp
int number = Convert.ToInt32(args["number"].ToString());

```

## bool
---
> `bool`is for `true`/`false`
{.is-info}
```csharp
bool boolean = Convert.ToBoolean(args["boolean"]);
```

## float
---
> `float`is for numbers with up to 7 decimals after the comma
{.is-info}
```csharp
float sevenDecimal = float.Parse(args["sevenDecimal"].ToString());
```

## double
---
> `double`is for numbers with up to 14 decimals after the comma
{.is-info}
```csharp
double fourteenDecimal = Convert.ToDouble(args["fourteenDecimal"]);
```

## decimal
---
> `double`is for numbers with up to 28 decimals after the comma
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