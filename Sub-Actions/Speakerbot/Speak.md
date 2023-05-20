---
title: Speak
description: How to pair up Streamer.bot and Twitch Speaker
published: true
date: 2023-03-27T18:36:00.251Z
tags: twitch, tts, speak, voice
editor: markdown
dateCreated: 2022-03-03T03:27:48.570Z
---

## Overview
Controls the Speaker.bot Speak Message using your Voice Alias

## Configuration
To do this select an Action you want to have this type of interactivity included then in the sub actions pane right click to bring up the menu now click `Add Action` then down to `Twitch Speaker` then click `Speak` now a dialog box will appear like the one shown below.

![speaker_options_.png](/twitchspeaker/speaker_options_.png =400x)

In this dialog box you will need to complete in order for streamer bot to pass data through to the Twitch Speaker application starting from the top is `Voice Alias` you will need to input a `Voice Alias` to tell the TTS what voice to use so for this example I’m going to use the default alias this can be found in the [Speaker.bot Application](https://streamer.bot). Open your Twitch Speaker application once loaded, click the `Settings ` tab and then click the `General` tab if it is not displayed already. It should look like this.

![twitch_speaker_application.png](/twitchspeaker/twitch_speaker_application.png =700x)

in this window look for the `Default Voice Alias` drop down and you will see the name of the Default voice remember this name as you will need to input this name into the Streamer.Bot Twitch Speaker dialog box. Next if you so choose you can pass the message through the bad word filter in the Speaker.bot application if you would like this to happen the please check the box next to this option.

Last step is the message box. You can either hard write the message in the box or pass a variable containing the message or even both. It’s up to you. Click the `Test` button for a preview, when you're happy with it click the `OK `button then `Save Setting & Viewers` button on the bot and you’re ready to go.  

![speaker_1_.png](/twitchspeaker/speaker_1_.png =400x)


> If you have already set up a different Voice Alias in the Speaker.bot Application then you can use this name instead.
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/Sub-Actions)
- [<img src="/logos/voicemod.png"/> **VoiceMod *Sub-actions reference for controlling VoiceMod***](/Sub-Actions/VoiceMod)
{.btn-grid .my-5}