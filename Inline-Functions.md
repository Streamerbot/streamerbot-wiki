---
title: Inline Functions
description: Reference of all Inline Functions
published: true
date: 2023-02-26T20:09:42.607Z
tags: 
editor: markdown
dateCreated: 2021-11-17T20:51:12.374Z
---

## Overview

These are the functions that are available when parsing most fields withing **Streamer.bot**, so anywhere you can do a `%variable%` replacement, you'll be able to do a `$function()$` as well.

All functions will also parse variable replacements within the function call itself, so if you have `$math(%x% + %y%)$`, the `%x%` and `%y%` will be replaced with there appropriate values before evaluating the math equation.

## Available Functions

* [<i class="mdi mdi-math-integral-box primary--text"></i> **<span>math(<i>&lt;math equation&gt;</i>)</span> *Basic and advanced mathematical functions***](/Inline-Functions/Math)
* [<i class="mdi mdi-format-text-rotation-none primary--text"></i> **<span>length(<i>&lt;text&gt;</i>)</span> *Determine the length of any variable or text***](/Inline-Functions/Length)
{.btn-grid .my-5 .list}

## Planned Functions

These are just a few functions that I do plan on adding, there is no timeline as to when they will be added, but they will be.

* [<i class="mdi mdi-google-chrome primary--text"></i> **<span>fetchurl(<i>&lt;url&gt;</i>)</span> *Fetch content from a URL***](/Inline-Functions/Fetchurl){.disabled}
* [<i class="mdi mdi-xml primary--text"></i> **<span>xpath(<i>&lt;xpath&gt;</i>, <i>&lt;json&gt;</i>)</span> *Parse XML with the XPath function***](/Inline-Functions/XPath){.disabled}
* [<i class="mdi mdi-format-horizontal-align-center primary--text"></i> **<span>substring(<i>&lt;string&gt;</i>, <i>&lt;start&gt;</i>, <i>&lt;length&gt;</i>)</span> *Get a certain part of a string***](/Inline-Functions/Substring){.disabled}
{.btn-grid .my-5 .list}
