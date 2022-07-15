---
title: Announcement
description: 
published: true
date: 2022-07-09T20:01:00.746Z
tags: announcement
editor: markdown
dateCreated: 2022-06-27T00:07:18.608Z
---

# Announcement

## Variables
| Value | Description |
|   ---:|-------------|
| `announceColor` | The color of the announcement, `DEFAULT`, `BLUE`, `RED`, `ORANGE`, `PURPLE`
| `message` | The announcement message
| `messageStripped` | The announcement message without emotes
| `emoteCount` | The number of emotes in the message
| `emotes` | The emotes in the message, this is a List<> object
| `badgeCount` | The number of badges for the user making the announcement
| `badged` | The badges for the user making the announcement, this is a List<> object

> This also contains the user's picked color, and user's months subscribed
{.is-info}

## C# Available Methods

```csharp
void TwitchAnnounce(string message, string color = null);
```

> Even though the color parameter is present, currently, due to a Twitch limitation, only null is supported, this will use the default announce command.  When Twitch fixes this, supported values will be `blue`, `orange`, `green`, `purple`
{.is-warning}