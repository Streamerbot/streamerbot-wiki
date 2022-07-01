---
title: Broadcaster
description: 
published: true
date: 2022-07-01T17:56:05.373Z
tags: 
editor: markdown
dateCreated: 2022-07-01T17:56:05.373Z
---

# Broadcaster

If Twitch is connected, actions will have the following five variables available to them

From version <span style="color:cyan">*(0.1.8+)*</span> you need to do a sub-action for this

| Variable | Description | Notes
|   ---:|-------------|
| `broadcastUser` | The Twitch display name of the broadcaster account |
| `broadcastUserName` | The Twitch user name of the broadcaster account |
| `broadcastUserId` | The Twitch user ID of the broadcaster account |
| `broadcastIsAffiliate` | Boolean value indicating if the broadcast account is a Twitch affiliate | `True` / `False`
| `broadcastIsPartner` | Boolean value indicating if the broadcast account is a Twitch partner | `True` / `False`