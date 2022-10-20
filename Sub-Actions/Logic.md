---
title: Logic Sub-Actions
description: Sub-Actions Reference
published: true
date: 2022-10-20T08:43:51.094Z
tags: subactions, logic, if, else, set argument, break, global variables
editor: markdown
dateCreated: 2022-06-28T00:50:33.068Z
---

Complex actions can be built using the logic operators in Streamer.bot. 

These will take data from various sources and evalutate them to direct the action, so understanding how they interact is key to building the workflow you want.

All logic in Streamer.bot must be performed against active Arguments. As any argument can only persist until the end of the running action if data need to be saved between actions, Global Variables can be used. Their data must be copied into an Argument to be usable

> Global Variables should always be stored in `camelCase` ie. with a lower case initial letter.
> Streamer.bot can not retrieve data from any store if the initial letter is capitalised.
{.is-danger}

> It is best practice to always name your `Arguments` something different than the `Global` you are reading from. 
> This will make your workflow easier to read and debug and can also prevent strange issues with logic and inline functions
{.is-warning}

* [<i class="mdi mdi-earth primary--text"></i> **Global (Get) *Read data from a`Global Variable` into an argument***](/en/Sub-Actions/Logic/Get-Global-Variable)
* [<i class="mdi mdi-earth primary--text"></i> **Global (Set) *Save data to a custom `Global Variable`***](/en/Sub-Actions/Logic/Set-Global-Variable)
* [<i class="mdi mdi-ab-testing primary--text"></i> **If / Else *Performs an `Action` if logical test is `True`***](/en/Sub-Actions/Logic/If-Else)
* [<i class="mdi mdi-variable-box primary--text"></i> **Set Argument *Store / Manipulate data in an argument***](/Sub-Actions/Logic/Set-Argument)
* [<i class="mdi mdi-close primary--text"></i> **Break *Diagnostic user only, cancels the running action***](/Sub-Actions/Logic/Break)
{.btn-grid .my-5}

Streamer.bot has 2 main variable types; `Global` and `Argument`

`Arguments` will only persist until the end of the currently executing action (or any Action called by it)
Sub-actions in the UI can only use `Arguments` as a data source

> C# can access an Action's active Arguments using the `args` directory 
{.is-info}

***

`Globals` will persist beyond the end of the action and are generally used to store data that needs to be read by future Actions

Their data can not be used directly in an Action. To use them a `Global (Get)` sub-action must be added to copy the currently stored data into a temporary argument. Subsequent sub-actions can then use this argument and data can be written back to Global storage using a `Global (Set)` sub-action.

> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/en/Sub-Actions)
- [<i class="mdi mdi-network primary--text"></i> **Network *Sub-actions reference for network requests***](/en/Sub-Actions/Network)
{.btn-grid .my-5}
