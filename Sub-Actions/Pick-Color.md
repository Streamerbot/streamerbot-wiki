---
title: Pick Color
description: Colour picker that populates variables for passing to OBS and HTML objects
published: true
date: 2021-11-19T20:52:23.237Z
tags: 
editor: markdown
dateCreated: 2021-11-19T20:36:22.012Z
---

# Pick Color
This subaction converts from a given color to a bank of variables that can then be passed to C# code, HTML object or any OBS source that is color aware

Variables list can be found [here](https://wiki.streamer.bot/en/Variables#pick-color)

***

![pick-color.png](/pick-color.png)

The Color picker will give the standard pallet picker so you can chose by a slider or by entering raw RGB / HSL values

Once a color is chosen the `Color` box will be populated with the RGB Hex value and `OBS Color` will populate with the raw integer value OBS expects for ABGR it uses for its natively supported sources.

Even without saving this sub action you can treat it purely as a calculator and just use these values directly in your effects, or you can define a `Variable Name` that will be populated at run time.

