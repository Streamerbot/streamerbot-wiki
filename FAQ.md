---
title: Frequently Asked Questions
description: Common Streamer.bot support & troubleshooting questions
published: true
date: 2022-11-10T16:32:48.887Z
tags: faq, support
editor: markdown
dateCreated: 2022-08-04T15:20:57.008Z
---

## General
### How do I install Streamer.bot?
**Streamer.bot is a portable application**.
Simply download the `.zip` file from the website and extract it to a folder of of your choice, then execute `Streamer.bot.exe` to start the application!
> The first time the program runs Windows may say the program is unsafe, this is normal behaviour for any application that Microsoft does not recognise. Simply choose Run Anyway to proceed.
{.is-warning}

### Why is Streamer.bot not opening?
There a couple of things that can cause this
1. Your `settings.json` file has been corrupted
   * If this has happend follow this guide below
   * [<i class="mdi mdi-backup-restore primary--text"></i> Backup & Restore Guide](/Backup)
2. You have moved/deleted/renamed files from your streamer.bot folder
   * If you have moved for example your `Streamer.bot.exe` file to your desktop, streamer.bot won't start. To fix this move the file back and if you lost that file download it download the files [here](https://streamer.bot)

### Why does my bot stop responding after I test a sub?
You have Sub Counter **enabled** in Streamer.bot and it is not pointing to a valid text file.  Either **disable** it or make sure the **file path** is pointing to a **valid** text file.

## OBS
### How do I upgrade to OBS WebSocket 5
1. Disconnect your OBS Connection but **don't delete it**
2. Edit the OBS Connection to version `v5.x` and port `4455` and make sure you have OBS Websocket version 5 installed.
   - If authentication is enabled in your OBS WebSocket settings, make sure the passwords still match.
3. And your done! Your sub-actions should behave fine.

**If you used OBS Raw then check this below ⬇⬇⬇⬇**
https://wiki.streamer.bot/en/Broadcasters/OBS/Requests
https://obs-raw.streamer.bot/

**If you did remove your OBS Connection, you can [Restore a Backup](/en/Backup)**