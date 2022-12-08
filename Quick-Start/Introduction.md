---
title: Streamer.bot Introduction
description: An introduction about all the fundamentals of Streamer.bot
published: false
date: 2022-12-08T08:35:34.037Z
tags: quick-start
editor: markdown
dateCreated: 2022-12-04T23:50:16.986Z
---

## Introduction
Welcome the Streamer.bot, a program that let you interactivly control your stream! At first it might seem a bit overwhelming, but after learning the fundamentals it easier then you might expect! There are four fundamentals Actions, Sub-Actions, Variables and events, on this page we'll guide you trough these.

## Actions
Actions is the place where all the data is stored for what you want to achieve, it's the thing that links everything together. In an action you will have all your [Sub-Actions](#sub-actions) and you link the action to [Events](#events) but to understand how an action works, we need to dive deeper in how the other fundamentals work.

## Sub-Actions
Sub-Actions are important to do all the stuff in the action, from sending messages to Discord to making your lights go red to playing some TTS. All of that you can imagine, you can do and if you can't you will be soon! Submit suggestions [here](https://ideas.streamer.bot).

## Variables
To make your Sub-Actions interactive you need Variables. Variables work with the name of the variable between percentage symbols e.g. `%variable%`. This variables are findable on this wiki. Variables primarily come from Events and Sub-Actions. You have Sub-Actions like [Get Random Number](/Sub-Actions/Get-Random-Number) where you get a random number between two values and it outputs it as a variable, in this case: `%randomNumber%`. But the majority of the variables comes from [Events](#events).

### Global Variables
Global Variables are for using variables in multiple actions with no time limit, the no time limit is when `Persisted` is turned on in Set Global Variable (this is by default) if you tick it of it resets when restarting Streamer.bot.
Global Variable example: You want to save your game in a global variable, you do this on the `Stream Update` event and do this below (this is how it should look in the Sub-Actions list, not in the Sub-Action itself):
```csharp
Set global "gameNameGlobal" to the value of %gameName%
Get global "gameNameGlobal" to "gameName", with default value of "No game available"
```
Now when using the Set Global Variable in the action linked to the `Stream Update` event. You can make a action with the Get Global Variable and use `%gameName%` as variable without it having to be linked to the event. 

### Action History
The action history is the place where you can see the variables that your action has generated. This tab is located at `Action Queues` `-->` `Action History`. When an action runs you can see it in the list there, if you want to disabled some events e.g. a chat message event, go to the actions tab and right click on the action and click on `Exclude from Hisory`. Back at the Action History you can right click on every item in the list and click on the `Inspect Variables After Run (#)` this will open a table displaying all the variables that you can use in the action.

## Events
Events come from Integrations, Broadcasters, Platforms, etc. e.g. Commands, Subscription, Heart Rate Event, Poll Updated, etc. when these trigger it will produce variables what you can find on the wiki, these variables are useable in Sub-Actions.