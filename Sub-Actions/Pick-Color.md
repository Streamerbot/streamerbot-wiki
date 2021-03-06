---
title: Pick Color
description: Colour picker that populates variables for passing to OBS and HTML objects
published: true
date: 2022-07-28T19:41:19.025Z
tags: 
editor: markdown
dateCreated: 2021-11-19T20:36:22.012Z
---

## Overview

Convert a selected color into a bank of variables that can then be passed to C# code, HTML objects, or any OBS source that is color-aware.

![pick-color.png](/pick-color.png)

## Configuration
### Colour / OBS Colour
The Color picker will give the standard pallet picker so you can chose by a slider or by entering raw RGB / HSL values

Once a color is chosen the `Colour` box will be populated with the RGB Hex value and `OBS Colour` will populate with the raw integer value OBS expects for ABGR it uses for its natively supported sources.

### Variable Name
Enter an alias for the resulting variables, outlined below.

## Variables

The following variables will be available after execution of this sub-action:

> In each of the following variables, replace `myColor` with the variable name you configured.
{.is-warning}

| Name | Description |
|-----:|:------------|
| `myColor.color.a` | The alpha value |
| `myColor.color.r` | The red value |
| `myColor.color.g` | The green value |
| `myColor.color.b` | The blue value |
| `myColor.html` | The html color code |
| `myColor.htmlalpha` | The html color code with alpha value |
| `myColor.obs` | The color as an OBS ABGR value |

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/en/Sub-Actions)  
- [<i class="mdi mdi-numeric primary--text"></i>**Get Random Number *Populate a variable with a random number***](/en/Sub-Actions/Get-Random-Number)
{.btn-grid .my-5}