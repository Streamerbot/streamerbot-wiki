---
title: Discord Basic Webhook
description: Discord Sub-Action Reference
published: true
date: 2023-02-11T18:38:49.295Z
tags: 
editor: markdown
dateCreated: 2022-10-16T17:08:15.813Z
---

## Overview
This is the first of a few new Discord specific sub-actions that will be added.  Up first is a friendlier way to post to a webhook you setup in your discord.  This one only allows for basic text posting.

Username, content, and image can contain variables and will be parsed.

Username, and image are also optional

![overview.png](/discord-basic-webhook-02.png =400x)

## Configuration
### Webhook Name
The name of the webhook (will be shown when you close this sub-action).

### Username
Optional username of the webhook in Discord. When not entered, the username will be the regular username as you've entered in Discord.

### Webhook Url
The webhook url that you've copied from this Discord.

### Content
The content of the message of the webhook, can use <kbd>Ctrl</kbd> <kbd>+</kbd> <kbd>enter</kbd> for multiple lines.

to ping a user or a role, you must set your discord application to Developer Mode. Click on the cog in left corner > Advanced > Toggle Developper Mode.

user: right click on the user icon , then click on Copy ID 
format to use in the message: `<@discordUserId>` e.g. `<@0123456789>`.

role: to get the id go to your server settings > role > right click on the role > copy ID 
format to use in the message: `<@&discordRoleId>` e.g. `<@&0123456789>`.

### Avatar Url
Here you can optionally fill out an URL to temporarily change the avatar of the webhook to something to your choose, an example use case for this is adding a Chat Message event and using the user's profile image in this field with the [Get User Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target) Sub-Action and then using the `%targetUserProfileImageUrl%` variable.

### Image
Optional added images the to webhook message.

### Text to Speech
Whether the Discord webhook message is Text to Speech or not.

---

- [<i class="mdi mdi-chevron-left"></i> **Discord Sub-Actions *Go Back***](/en/Sub-Actions/Discord)
{.btn-grid .my-5}