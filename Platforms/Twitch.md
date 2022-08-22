---
title: Twitch
description: Configure Twitch as a streaming platform in Streamer.bot
published: true
date: 2022-07-28T19:32:17.735Z
tags: twitch, guides, platforms, configuration
editor: markdown
dateCreated: 2021-08-25T21:34:42.553Z
---

![twitch-logo.png](/logos/twitch-logo.png){.align-abstopright}

## Quick Links
- [<i class="mdi mdi-creation text--twitch"></i> **Twitch Event Reference *Click here for the full list of all Twitch events and variables***](/en/Platforms/Twitch/Events)
- [<i class="mdi mdi-lightning-bolt-outline text--twitch"></i> **Twitch Sub-Action Reference *Click here for the full list of all Twitch sub-actions***](/en/Sub-Actions/Twitch)
{.btn-grid .my-5}

## Overview
Streamer.bot integrates directly with Twitch to offer a set of first-class functionality.

## Configuration
You can configure both a **Broadcaster** *(required)*, and a **Bot** account *(optional)* for interacting with Twitch services.

![twitch-accounts-019.png](/twitch-accounts-019.png =800x)

- [<i class="mdi mdi-transit-connection-variant text--twitch"></i> **Twitch Account Connecting issues**](/en/Sub-Actions/Twitch/Accounts){.disabled}
{.btn-grid .my-5}

### Broadcaster Account
A Broadcaster account is **required** to monitor your Twitch chat and receive all Twitch [events](/en/Platforms/Twitch/Events).

1. Press `Connect to Twitch` to sign in to your Twitch account and retrieve an OAuth2 token.
2. `Auto Connect` will set Streamer.bot to connect to twitch with the defined account on startup
3. `Auto Reconnect` instructs Streamer.bot to attempt reconnection in the case of any network interruption to the platform


### Bot Account
By default any [sub-actions](/Sub-Actions#main) will be sent through the Broadcaster account. If you want a secondary account to send these actions / messages it can be defined here in the same way


### Refresh Categories
Use this to pull a current list of available Twitch categories to be used as variables in [sub-actions](/Sub-Actions).

For example, you could automatically change scenes in [OBS Studio](/en/Broadcasters/OBS) if your Twitch category is changed to a specific game.

    
- [<i class="mdi mdi-chevron-left"></i>**Platforms *Go Back***](/en/Platforms)
- [<i class="mdi mdi-twitch text--twitch"></i>**Twitch Events *Up Next***](/en/Platforms/Twitch/Events)
{.btn-grid .mt-10}
  