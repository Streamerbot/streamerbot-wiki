---
title: Generic Variables
description: Variables Reference
published: true
date: 2023-04-25T17:21:30.483Z
tags: variables, reference
editor: markdown
dateCreated: 2022-06-30T19:57:33.363Z
---

## Overview
Generic variables are always available to most event sources, so consider these the bare minimum you can use in your [Sub-Actions](/Sub-Actions)

## General
Useful general purpose variables{.subtitle}

Name | Description
----:|:------------
`date` | Current system date <br> *Accepts any standard formatting notation eg. `%date:yyyy/MM/dd%` or `%date:dddd, dd MMMM yyyy%`*{.small}
`time` | Current system time <br> *Accepts any standard formatting notation eg. `HH-mm`*{.small}
{.vars-table}

## Event Source
Variables related to the triggering event source{.subtitle}

> These variables aren't strings and thus **cannot** be used in if statement Sub-Actions. To compare these values C# is needed with the usage of the [appropriate types](/Sub-Actions/Code/CSharp/Available-Methods/General#source-event-type)
{.is-warning}

Name | Description
----:|:------------
`__source` | The name of the event triggering the action
`eventSource` | Value to specify which platform generated the event <br> `twitch` or `youtube`
{.vars-table}

## Action
Variables related to the action being called{.subtitle}

Name | Description
----:|:------------
`actionId` | The unique ID number of the first action called
`runningActionId` | The instance ID number of the action in the queue
{.vars-table}