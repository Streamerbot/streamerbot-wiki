---
title: Variables
description: Reference of all variables/arguments that may be available in Streamer.bot events and sub-actions
published: true
date: 2022-12-06T15:57:55.778Z
tags: variables, arguments
editor: markdown
dateCreated: 2021-08-25T21:34:50.460Z
---

## Overview
All [events](/Events) in Streamer.bot will generate an **argument stack** specific to that event source, providing variable data to the current action, and subsequent [sub-actions](/Sub-Actions).

Most events will always include all generic arguments in addition to their own documented variables. Any exceptions will be listed on the page detailing that function.

**This list is not exhaustive and some variables may work with sub-actions / events even though they do not specifically state compatibility.**

> If an event is not documented, you can always use [Log All Arguments](/Sub-Actions/Code/Execute-CSharp-Code/Examples/Log-All-Arguments) in a sub-action to see all variables available to you.
{.is-info}


## Usage
Variables can be used in most [sub-action](/Sub-Actions) text inputs.

To use a variable from the current argument stack, wrap the variable name with a `%` symbol, e.g. `%userName%`

### Tips
- Arguments only persist until the called action finishes execution and can not be referenced by any other action
	- If you want to share variables across multiple actions you can write them out to a [Global](/Sub-Actions/Logic/Set-Global-Variable) variable{.small}
- Variables are added onto the argument stack during execution of each sub-action
  - If you are testing and a variable seems to be missing, ensure you are testing at the right point of execution{.small}
- You do not need to wrap variable names with `%` within logic statements like `If` and `Global`
  - This was required in older versions of Streamer.bot{.small}
  - Wrapped variable names will still work as normal in this context{.small}


### Formatting
> Variables can be formatted inline using standard C# notation
{.is-success}

For example, to format a numeric veriable `%tipAmount%` as a currency with 2 decimal places, we can use the following syntax: `%tipAmount:c2%`

Similarly, `%time%` can be formatted in short notation with AM/PM using the following syntax: `%time:t%` 

Further information on valid formatting modifiers can be found [here](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings) and valid format strings for `%time%`

### Inline Functions
> Anywhere you can do a variable replacement, you can also execute [Inline Functions](/Inline-Functions)
{.is-success}

## Variable Sources
- [<i class="mdi mdi-variable-box primary--text"></i> **Generic Variables *Available to most triggers automatically***](/Variables/Generic)
- [<i class="mdi mdi-creation primary--text"></i> **Events *All events and their associated variables***](/Events)
- [<i class="mdi mdi-lightning-bolt-outline primary--text"></i> **Sub-Actions *Some sub-actions will also generate variables***](/Sub-Actions)
- [<i class="mdi mdi-comment-alert primary--text"></i> **Commands *Variables from triggered chat commands***](/Commands#variables)
- [<i class="mdi mdi-triangle-outline primary--text"></i> **Pyramids *Variables related to chat pyramids***](/Settings/Pyramids)
- [<i class="mdi mdi-file-document-multiple primary--text"></i> **File/Folder Watcher *Variables from monitored files & folders***](/Settings/File-Folder-Watcher)
- [<i class="mdi mdi-account-heart primary--text"></i> **Sub Counter *Variables from sub counter settings***](/Settings/Sub-Counter)
- [<i class="mdi mdi-comment-quote primary--text"></i> **Quotes *Variables from the built-in `!quote` command***](/Settings/Quotes)
- [<i class="mdi mdi-account-voice primary--text"></i> **Voice Control *Variables from all Voice Control actions***](/Voice-Control#variables)
{.btn-grid .my-5}