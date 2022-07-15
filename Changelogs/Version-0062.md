---
title: Version 0.0.62
description: 
published: true
date: 2022-07-09T19:56:24.113Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:52.157Z
---

Visit [Streamer.bot 0.61](Version-0.61) to see all the shiny new features and updates.

Just a small fix

* Fix double clicking on commands
* Possible startup error fix
* Fix strange behaviour with new control used for grouping in actions/commands

**NOTE**
Windows Defender may give a false positive, I believe this is due to the inclusion of the Roslyn compilers which power the C# compiling capabilities. The fact they're there and there is code within the app to compile stuff itself I believe is what's causing the flagging, I'm not sure how to remedy this.