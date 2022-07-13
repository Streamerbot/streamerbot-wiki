---
title: Twitch
description: 
published: true
date: 2022-07-13T20:14:39.975Z
tags: twitch, platforms
editor: markdown
dateCreated: 2021-08-25T21:34:42.553Z
---

![twitch-logo.png](/logos/twitch-logo.png){.align-abstopright}

## Quick Links
- [<i class="mdi mdi-creation text--twitch"></i> **Twitch Event Reference *Click here for the full list of all Twitch events and variables***](/en/Platforms/Twitch/Events)
- [<i class="mdi mdi-lightning-bolt-outline text--twitch"></i> **Twitch Sub-Action Reference *Click here for the full list of all Twitch sub-actions***](/en/Sub-Actions/Twitch)
{.btn-grid}

## Overview

Streamer.bot can integrate directly with Twitch! to bring a new level of interactivity to your stream. Details on how to configure your accounts and the different options available to you through the platform will be detailed on their own pages linked below.

## Configuration

![twitch-accounts-019.png](/twitch-accounts-019.png)

### Broadcaster Account

If you want streamer.bot to be able to monitor chat and Twitch! events, a `Broadcaster` account must be defined

Press `Connect to Twitch` to automatically obtain a token 

`Auto Connect` will set streamer.bot to connect to twitch with the defined account on startup

`Auto Reconnect` instructs streamer.bot to attempt reconnection in the case of any network interruption to the platform

***

### Bot Account

By default any [sub-actions](/Sub-Actions#main) will be sent through the Broadcaster account. If you want a secondary account to send these actions / messages it can be defined here in the same way

***

### Refresh Categories

Use this to pull a current list of available Twitch categories. These can be used as variables in [sub-actions](/Sub-Actions#main) for example to change scene if category is changed to a specific game

* [Accounts *Configuration of Twitch **Broadcaster** and **Bot** accounts*](/en/Platforms/Twitch/Accounts)
{.links-list}