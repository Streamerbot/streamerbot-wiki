---
title: Broadcaster
description: 
published: true
date: 2022-07-03T18:05:08.163Z
tags: 
editor: markdown
dateCreated: 2022-07-01T17:56:05.373Z
---

# Broadcaster

If Twitch is connected, actions will have the following five variables available to them

*v0.1.5-v0.1.7*{.version-badge} This functionality is automatic
*v0.1.8+*{.version-badge} Requires the [Add Broadcaster Information](/en/Sub-Actions) sub-action because YouTube integrtion was added

| Variable | Description | Notes
|   ---:|-------------|
| `broadcastUser` | The Twitch display name of the broadcaster account |
| `broadcastUserName` | The Twitch user name of the broadcaster account |
| `broadcastUserId` | The Twitch user ID of the broadcaster account |
| `broadcastIsAffiliate` | Boolean value indicating if the broadcast account is a Twitch affiliate | `True` / `False`
| `broadcastIsPartner` | Boolean value indicating if the broadcast account is a Twitch partner | `True` / `False`