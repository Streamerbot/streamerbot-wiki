---
title: Quick Start Guide
description: A Few Quick Tips and Examples to get you started
published: true
date: 2022-07-03T16:20:58.570Z
tags: guides
editor: markdown
dateCreated: 2022-01-20T12:18:32.710Z
---

# Overview
This page is dedicated to getting your bot up and runninag as fast as possible. 

If you are new to local bots and want to learn about the bot while installing some pre-configured (but still awesome) content then you might want to take a quick side trip to [VRFlad's Fasttrack](https://vrflad.com/fasttrack). Don't worry, the wiki will be here when you get back.

For the more advanced users that want to start off with a clean slate and start building, then by all means... read on!

# Getting Started
## Connecting your Twitch account!
![connect_to_twitch_.png](/quick-start/connect_to_twitch_.png =800x)
1. Navigate through the following: `Platforms` ---> `Twitch` ----> `Accounts`
2. Press the `Connect to Twitch` button to bring up an authorization webpage that will detail all the permissions **Streamer.bot** wants to have access to on your behalf

> You can not type into either of the username boxes. They will display your username once you have authenticated.
{.is-warning}
### Broadcaster Account

If you want Streamer.bot to be able to monitor chat and Twitch events, a `Broadcaster` account must be defined. 

Press `Connect to Twitch` to automatically obtain a token. If you are already logged in on your web browser you will be taken immediately to the permissions screen. This is a list of all the Twitch features the application will be able to perform in your name. If it is not listed here, the bot can't do it, even if you could perform an action by typing a command in chat yourself for example.

If the logged in user is not the one you wish to use, please log out and enter the credentials you wish to use 

> `Auto Connect` will set **Streamer.bot** to connect to Twitch! with the defined account on startup
{.is-success}

### Bot Account

You might wish for messages sent to chat to be sent from a separate user account. You can log in such an account here the same way as the Broadcaster account.

The account can be any standard Twitch account but with the permission scope the application requests it can not listen to incoming events or messages, it can only send messages to chat or whisper.

> Sending whipsers programatically is something that `Twitch` restricts fairly heavily.
If the chosen account is not more than **12** months old, or already pre-verified as a **bot** you will not be able to send whispers from the application
{.is-warning}

> If you you do not intend to use a bot account, leave this field blank or you will restrict certain actions from working correctly such as responding to chat commands that the bot has written in chat
{.is-success}

Once you have a bot account configured, you can select which account should send chat messages on a per [sub-actions](/Sub-Actions#main) level. 

---

## Connecting OBS / Streamlabs Desktop

## Streaming Software {.tabset}
### OBS
To enable remote control of your `OBS` from **Streamer.bot** you will need to first install the OBS Websocket Plugin
> OBS Websocket v4.x is the only supported version at this time, v5.x requires a re-write and is being worked on, but is still missing capabilities
Download OBS Websocket plugin [here](https://obsproject.com/forum/resources/obs-websocket-remote-control-obs-studio-from-websockets.466/)
{.is-warning}

Once this is installed, configure your port settings and password if you want one inside OBS. You will need to match these settings in Streamer.bot
![WebsocketSettings](https://lh3.googleusercontent.com/-VCh9WVIx1ZI/YPtSPtSppaI/AAAAAAAAEA4/OK-jMEvnI3YAXDRBpLPhO8lG1V6jimZOwCLcBGAsYHQ/image.png)

---

Go to the OBS tab, Once configured, connected OBS sessions will report their status on this screen.

![obs_event_01_.png](/quick-start/obs_event_01_.png)

To add a new connection, `Right-Click` -> `Add` to open the new connection dialogue
![New Connection](/119574587-9adb7e80-bdad-11eb-82c1-ec9ed668a40d.png)

Give it a name and set the IP address and Port number of the OBS Websocket
The Default values of `127.0.0.1` and `4444` will look for the out-of-box configuration for OBS installed on the same computer as Streamer.bot is running

`Password` Will not be required unless you have specified one in OBS

> Connections can be configured to `Auto Connect on Startup`, and to `Reconnect on Disconnect` with a retry interval you specify in seconds
{.is-success}

### Streamlabs Desktop
While **Streamer.bot** does support the use of `Streamlabs Desktop`, it is highly recommended by most users to use `OBS`.

This section will be updated with information, but is near identical to the OBS setup.

## Chatbot Response Examples

If you are coming from another platform you are probably used to having some basic commands your bot can respond to. 
Streamer.bot does not have those out of the box but it can do most of the common replies with a few simple actions that can be customised how you like it.

Below you will find code to import them directly into your setup for immediate use and also explanations on why the workflows are set up this way so you can build more advanced actions if you want them.

## {.tabset}
### Examples
![ActionExamples](https://media.discordapp.net/attachments/880176943566299136/933519049042825216/unknown.png)
### Import Code
```
TlM0RR+LCAAAAAAABADlWltvK7cRfi/Q/7AxoLfwmPfLeTtIgaBAG7TpSV+KohiSQ0uIrFV3V3aMNP+9w10rlmQf1JIvsJsn7ZJLLvnNfDPfcPXz73/XNGdX2PWLdnX2sRFfjw0ruES6O/vrZpF+bP42QDecTT2QBnqyp85/1Pum+Xn6oa5FrkOUA5u9UywlbpiOUJg31jNtEnAeQ5I5TnONg/69wU191WqzXN614griEut8Q7fBu/btur7qBxj6nWkuunazPlhx8z3263aVcPdBWF7DTf/9pm62wLLfmbyDVW4vP40bvN+baKZN1+FquN93D5Q9YMZHNt2yLm8+DOv+4/k5rBcfUrdZpfmaXvvjhxUO58P1Ykjz86sFXmOX2s1qOJ/FroWcoB9+6LH7jnY/u9vLOO8VdIuK1Xe3yEyjv6mjD56czJPRanA8MK5BM52kYLFAJht57rl2PqR0MPAaFxfzumv+ge/3DDfr+lLBudvv2Jpjz6rTKlYZf6pz3bX+8vUjQcuYKm6XuIVqsx4WdHc8StPABwFSmDEHGZkUQF4LRVZsCosQkonFKlHCawAkngOgCzgJnsubb+EL8HCpEJxIzAsQTAePDBIohtpG9EYj9/Y14JHPAc+wGJan4fO5jnwQIOdTiMULViQn/xEiswDJslCIeiCzlSa/BkDqMQAN+FN971k198dmNtl91vynGfc3toxXs4bafhhJQ40Te+pjfx+jTU9tO3HnEL11hwUpcuZPaYxqdaMPIQcass7KMh8gMp09sCDpihNoaKKXNpXjkTsWN72D2/byn4eh/ts6zRjvd7pSu1zCuse80zt1bg1wmCuDyVFFxBqHA9MFE5HJFhYyeUsOOmTBn54rD4Pdu0uWrxL3eSH3SmiZixTdtBGB+VwCSwpsiDKg4+bNJMYtb/cRmDVz6Bvyp1WzXFxhU9ruV7KeyEkTZRRBO1ZMcuShVrOgrGOUApRUVc1p9/KcFK/ISZuC02A0c2gpwWVSsqE4y6R13nHuQRr5dE6+N0ZuHe7zHJu69mbRN7fzLW+a2ZQPRn/b98gT3S5lUE5S6SCV4JREnSb9FTWDDM5KKWzmJyTRp1Dxpd1O5ViU4a5GHtLlQhrmueEs5SJRRieVeYayKcPwbt2urv3A7WrTc7qd8EJT0iVJmzlO2g3AAeMJERLnAPkE7f+W3Q6FDaS5kCFSwtOOrnwOiYkQNTdee23g6W5XaF1tFYrvyfceX7FP2xs963hJssXmyyW7MJxykvcMIhqyUdbMp6xYNEWjdlgoKb15ZXLH2qpRZnu7rhS+5yDjbI+WKYKwyaRQlNRUOoSILPAArFDBnqLTOctD1ffOZYqLHq3DwMpYLIlE7iEcZwKsS55qTQ/m2Yib3xNv+3bTJfw8GZE/TL66/ge55kPMMiKRqxTJtOeBkf6lOl6REJEplpCO1rtGvCzTNiPBbtrNlkb5MB027WpLuT/UlHkiyzDpIgAl1aeCwImJroxWzAnpBbhEqeSEs5+3zDJplbExGGapJGfaKirQHdUGEAFQEMuKz8/FssXq4jdDM6uUJgwTK0IppmV2zAP3TFnhqcmpFI+O169HszlQcR2pyv7VcPcIN2rSqfvTBf6pXV2cSjpbIBSfqB61hJIGVageNYYJyvqWaiETUf9/kQ4EzwW4Yc5Q+NVUGLFR/nCRXcrkNUqXp5MudUih8P1mNnEk5YSM4LWluM2FZRqpwPEQE90WU+seIfjRfmSeVNt8kXKPV96jEQm28xkZ6wIfLP4OBTdMfPvm0P47WPlUZPShMBmiYFpTRR5AIlPBBmNMylnx11Dcj/oGtFsj3+5tCj87kDTXJLpvPX4UA/sgnH5i73I0CqheJv2pKf+zyk5mtAkUyhF9fAVBsPsp6KVjk1dSIEVcxn09ti+J097Rk+z2kEuJ2ulnOB3s299MWEIRkqoKyxifKRiR90RlJIsRA4X+BIYf/dHnhcLSlmh/WSL02Fy0TZojWaTdDPtkg6HZxq4pTn0YrnYj1Hgs0LDmj82yJSUxzPGyIQON2qKft5tlboa2/erUs1OpRAoUrYArCl7GBwr0VMwUNDFbgOjyCccFb1kw6FBK1kRKr5ShUq1eZScZtxmE4oZr+QyHWAPC5Xui5eOzaN3Zvy7xMmLXn88Wq/Vm4P8ri9Yxf56GPMhr8GikSKTrs071YJECJQAJ2EimCUUXxV/lbxSPYvYVLEePoPkg9g00y0U/NG1p6i6bW2Sa0rWXTXWH3Oz7ws62OReYMsR6DsPr3yMcA7SaySRN1jG6qE44iOLhTdCv/kxPThzadv7yX0FA6thGJgAA
```
