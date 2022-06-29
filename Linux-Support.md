---
title: Linux Support
description: Information pertaining to running Streamer.bot on Linux
published: true
date: 2022-01-29T16:30:29.276Z
tags: 
editor: markdown
dateCreated: 2021-10-24T01:57:25.992Z
---

# Linux Support

Stay tuned for more information

## Installer

There is an install script available at: https://github.com/Streamerbot/sb-linux-installer

[Installation Guide on how to install on Linux can be found here](/en/Installing-on-Linux)

## Updating Streamer.bot on Linux
To update Streamer.Bot on your linux install you need 2 simple commands 

Open a Terminal Window issue the following commands 

```bash
cd sb-linux-installer 
UPDATE=1 ./install.sh
```

wait for it to complete and congratulations you have sucessfully updated Streamer.bot

## Experimental Linux Support

> There is no guarentee this will work 100%, there are areas of the app that may not function correctly, so this will be a complete work in progress depending on time/effort.
{.is-warning}

It is possible to run this current version (**0.1.5**) using wine/wine64 within Linux

The entire network stack was re-written to make this possible, as it was a major blocker.

I've been doing some tests using the staging version of Wine, which is v6.19 in Ubuntu 20.04 LTS.

For your Wine setup, you'll want the following:
```bash
winetricks dotnet472
winetricks d3dcompiler_47
winetricks dxvk
```
You will also want to make sure gnutls (for 32-bit: lib32-gnutls) is installed.

This information should also apply to TwitchSpeaker, ~~one area that will not work in TwitchSpeaker are SAPI5 voices~~, and the Azure voices may also not work. Again, this is very experimental.

For SAPI5 voices you need to setup SAPI5 with:
```bash
winetricks sapi
```
As well as installing the SAPI5 voices you want to use.

A dedicated page on the wiki will likely be created for those who are using/testing it under Linux to list what works and what the current issues are.

> Running **Streamer.bot** and/or **TwitchSpeaker** under Linux is considered to be experimental, so expect bugs/issues.
{.is-warning}

## Known issues

### Right click viewers

Right click on viewers on the Viewers tab does not render correctly, you need to move the mouse over the opening context menu to let it appear. The speed with which the menu shows up can be improved by redirecting stderr (and stdout) to /dev/null:
```bash
wine Streamer.bot.exe >/dev/null 2>&1
```
The rendering issue seems to be fixed with wine 7

### Grouping of actions
Though actions and commands can be grouped, the corresponding lists don't show any groups. All actions and commands are just listed in the order they have been added.