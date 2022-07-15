---
title: Version 0.0.63
description: 
published: true
date: 2022-07-09T19:56:27.425Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:56.021Z
---

Visit [Streamer.bot 0.61](Version-0.61) and [Streamer.bot 0.62](Version-0.62) to see all the shiny new features and updates.

Some fixes/changes

* Log files have been moved to their own logs folder
* All settings and cache files are now in their own data folder
* Change what modules are merged
* Tweak finding references for Execute C# code
* Fix delete key not removing references properly in Execute C# Code sub-action
* Fix OBS/SLOBS visibility state not setting a default state, which could lead to a crash
* Commands became unusable after editing a command, woops
* Added 2 new scopes, to create clips, and to manage your broadcast (update title, set game, etc)  The app will notify you that you'll need to re-auth
* Added new Action Added/Updated/Deleted events, mostly to better support StreamDeck plugin
* Misc fixes/etc that I've probably forgot
* Add top/bottom move otpions for moving sub-actions
* Fix creating rewards not having action assigned if one was chosen
* New app icon

## StreamDeck
Was tinkering around with StreamDeck plugins and managed to get a basic one working, you can create a new button and give it an action.  My experience with writing these plugins is very limited, so this version may not advance very far, but hopefully a more advanced one may eventually takes its place.

[StreamDeck Streamer.bot](https://github.com/nate1280/streamdeck-Streamer.bot)

## Logs and Settings
When starting Streamer.bot without a logs or data folder, it will auto-create these folders, and move any existing logs and settings into this folder for you, and carry on like normal.

## EXE Changes
You'll notice that the archive is a bit large, and contains more files now.  I've decided to split all System/Microsoft libraries out of the merge and will now be alongside the application.  I'm hoping that this might reduce the number of false positives in anti-malware applications.

## Execute C# Code
Finding refs for Execute C# has been improved, and seems to do a better job at finding system related references, this is still an ongoing tweaking.

This also occurs during an import when a C# sub-action is found, it will re-find references for your local system and update them, there still may need to be manual finding of refs, and the import/export process will likely improve for these scenarios (i.e. including external libraries, and more)