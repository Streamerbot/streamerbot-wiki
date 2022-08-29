---
title: Quotes
description: Configure Streamer.bot's built in !quote command
published: true
date: 2022-07-15T18:23:44.009Z
tags: commands, settings, quotes
editor: markdown
dateCreated: 2021-08-25T21:32:14.446Z
---

**Streamer.bot** has a built in quote system.

> You must have a category set to add quotes to the quote system, otherwise it tries to set null data which can cause a crash or invalid data structure
{.is-danger}


![quotes.png](/quotes.png)

## Twitch commands 
The following twitch commands can be used to add, remove and to retrieve the quotes
```
!quote add <string>
!quote del #
!quote
```
Please note, the add and remove commands need the permission level as defined in the setting Perm to Add.

## Example messages to be used in actions for quote addition / removal
Quote addition message
```
%user%, quote has been added as #%quoteId%
```
Quote output message
```
#%quoteId%: %quote% [%quoteUser%, %quoteGame% at %quoteTime%]
```

## Additional use of the quote system
![Quote Action](/123520512-082e4800-d6a9-11eb-95f9-e5c016b42f21.png)

You can automate the retrieval of a specific or random quote using the Get Quote Action. Once retrieved, you can reference the quote using the variables shown above in the Quote output message.

## Variables

When using the built-in `!quote` command the following variables will be made available:

Name | Description
----:|:------------
| `quote` | The quote content
| `quoteID` | The quote ID number
| `quoteUser` | The user that added the quote,
| `quoteGame` | The game the broadcaster was playing at the time
| `quoteTime` | The date it was logged