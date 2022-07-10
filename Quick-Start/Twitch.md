---
title: Quick Start - Twitch
description: Connect your Twitch account with Streamer.bot
published: true
date: 2022-07-10T01:25:27.617Z
tags: twitch, guides
editor: markdown
dateCreated: 2022-07-10T01:25:27.617Z
---

# Connecting your Twitch account!
![connect_to_twitch_.png](/quick-start/connect_to_twitch_.png =800x)
1. Navigate through the following: `Platforms` ---> `Twitch` ----> `Accounts`
2. Press the `Connect to Twitch` button to bring up an authorization webpage that will detail all the permissions **Streamer.bot** wants to have access to on your behalf

> You can not type into either of the username boxes. They will display your username once you have authenticated.
{.is-warning}
## Broadcaster Account

If you want Streamer.bot to be able to monitor chat and Twitch events, a `Broadcaster` account must be defined. 

Press `Connect to Twitch` to automatically obtain a token. If you are already logged in on your web browser you will be taken immediately to the permissions screen. This is a list of all the Twitch features the application will be able to perform in your name. If it is not listed here, the bot can't do it, even if you could perform an action by typing a command in chat yourself for example.

If the logged in user is not the one you wish to use, please log out and enter the credentials you wish to use 

> `Auto Connect` will set **Streamer.bot** to connect to Twitch! with the defined account on startup
{.is-success}

## Bot Account

You might wish for messages sent to chat to be sent from a separate user account. You can log in such an account here the same way as the Broadcaster account.

The account can be any standard Twitch account but with the permission scope the application requests it can not listen to incoming events or messages, it can only send messages to chat or whisper.

> Sending whipsers programatically is something that `Twitch` restricts fairly heavily.
If the chosen account is not more than **12** months old, or already pre-verified as a **bot** you will not be able to send whispers from the application
{.is-warning}

> If you you do not intend to use a bot account, leave this field blank or you will restrict certain actions from working correctly such as responding to chat commands that the bot has written in chat
{.is-success}

Once you have a bot account configured, you can select which account should send chat messages on a per [sub-actions](/Sub-Actions#main) level. 
