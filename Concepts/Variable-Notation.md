---
title: Variable Notation
description: Guide on how to use the Streamer.bot variable notation
published: true
date: 2023-05-09T22:02:01.769Z
tags: 
editor: markdown
dateCreated: 2023-05-09T22:02:01.769Z
---

## Overview
All Streamer.bot variables are parsed from a JSON object, you can access this object in C# with the [args dictonary](/Sub-Actions/Code/CSharp/Streamerbot-Variables). But in normal Sub-Actions you can use the parsed version with `%%`'s.

In this guide we'll show you on how all the variables from the documentation and from the JSON work.

## Type 1
### Examples
* `%line#%`
* `%poll.choice#%`

### Guide
Here you see two variables with multiple numbered variations. The `#` means a number reaching from 0 to the end of the list. So if you have 3 lines the variables will be `line0`, `line1` and `line2`.

## Type 2
### Examples
* `%user%`
* `%poll.duration%`

### Guide
Here you see two variables in a pure object form. Object are parsed with `.`'s so an object of poll with duration will be `poll.duration` and the default object with user will just be `user`.