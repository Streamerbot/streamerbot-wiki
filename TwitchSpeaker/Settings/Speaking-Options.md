---
title: Speaking Options
description: TwitchSpeaker Speaking Options 
published: false
date: 2023-01-18T23:52:37.060Z
tags: twitch, tts, settings, twitchspeaker, options
editor: markdown
dateCreated: 2023-01-10T02:25:56.142Z
---

## Overview

TwitchSpeaker has many speaking option as seen in the screenshot below but each section will be explained and the intented functions. To get to this tab you will need to navigate through the following tabs on the first row click the `Settings` tab then click the `Speaking Options` tab.

![tts-speakingoptions.png](/twitchspeaker/tabs/settings/speaking-options/tts-speakingoptions.png =700x)

## Configuration
### Speaking Options 
In this section you will find most of the control in this tab. 

The `Say everything` option can be Enabled or disabled so when this option is enable TwitchSpeaker will say everything in chat unless the chatter/user is on the ignored list. When this option is disable the user/chatters are required to use the `TTS Speaking Commands` that you have set in that section (this will be explained later) but default it is either `! or !say` before the message for twitch speaker to speak this. 

The `Say Username` option again the same enable / disable options . When enabled is will speak the username of the message being spoken  and if this is disabled the username is skipped  however, this option does have a post fix which you can edit by changing the text in this field by default it is set to `said`  Example: "Omnidreamer said Hello". This is the example if this option is enabled but if this is disabled twitch speaker it would just say "Hello".

The `Sticky Random Voice`. this make the first random voice chosen by twitchspeaker is assigned to the user when they have spoken.

The `Allowed Forced` option allows forced TTS messages.

The `Only say username if previous was different` will ignore users that trigger TTS right after they triggerd TTS.

The `Replace %name% with nickname if available` will replace the username in the TTS to a nickname (if it's available).

The `Last spoke grace period` is a cooldown on TTS.

The `Max Words` is a limit on how may words TTS can contain.

The `Not Allowed Text` is the message that will be send to chat if a user isn't allowed to use that TTS.

The `URL Filter` will filter URl's from the TTS, you can choose from `Disabled` (doesn't filter the URL), `Strip` (removes the URL from the TTS) or `Yeet All` (will remove the entire TTS).

### Stop and Skip spoken messages on
Here you can choose to skip messages if message is deleted, user is timed out or user is banned.

### Command Option
The `Silence Command Output` will silence the output of the command.

### Permissions
General permissions for who has access to TTS.

### Emotes
If you want to ignore emotes from certain sevices and/or only allow the first emote.

You can also specify allowed emotes, this will bypass the filters set previously.

### TTS Speaking Commands
Commands that can be used in chat to use TTS.

### Ignored Prefixes
Ignores TTS where the message is prefixed with certain characters.

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/TwitchSpeaker)
- [<i class="mdi mdi-content-cut text--twitch"></i>**Replacement *Add a bad words filter or use regex to replace words.***](/TwitchSpeaker/Settings/Replacement)
{.btn-grid .my-5}