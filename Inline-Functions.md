---
title: Inline Functions
description: 
published: true
date: 2022-07-15T19:16:33.250Z
tags: 
editor: markdown
dateCreated: 2021-11-17T20:51:12.374Z
---

## Overview

These are the functions that are available when parsing most fields withing **Streamer.bot**, so anywhere you can do a `%variable%` replacement, you'll be able to do a `$function()$` as well.

All functions will also parse variable replacements within the function call itself, so if you have `$math(%x% + %y%)$`, the `%x%` and `%y%` will be replaced with there appropriate values before evaluating the math equation.

## Available Functions

* [Math *Basic and advanced mathematical functions*](/inline-functions-math)
{.links-list}

## Planned Functions

These are just a few functions that I do plan on adding, there is no timeline as to when they will be added, but they will be.

* fetchurl(\<url\>)
* xpath(\<xpath\>, \<json\>)
* substring(\<string\>, \<start\>, \[length\])
{.links-list}