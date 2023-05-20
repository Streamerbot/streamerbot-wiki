---
title: Get Quote
description: General Sub-Actions Reference
published: true
date: 2023-03-27T18:36:00.251Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:33:26.393Z
---

## Overview
Add variables from a specific or random quote to your arguments

## Configuration
### Type
The type can either be `Random` or `Specific`, if `Random`, a random quote will be picked from your available quotes, and added to the arguments

### Quote Id
Available when you have the `Type` set to `Specific`, you can specify the exact quote number to be added to the arguments

## Variables
Name | Description
----:|:------------
`quoteTime` | The time that the quote was made
`quoteId` | The numeric id of the quote
`quoteUserId` | The user id from the account that made the quote
`quoteUser` | The user's display name from the account that made the quote
`quotePlatform` | The platform from the account that made the quote <br> `twitch`/`youtube`
`quoteGameId` | The game id from the quote
`quoteGame` | The game name from the quote
`quote` | The quote itself

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/Sub-Actions)  
- [<i class="mdi mdi-keyboard-close primary--text"></i>**Keyboard Press *Simulate keystrokes***](/Sub-Actions/Keyboard-Press)
{.btn-grid .my-5}