---
title: Streamer.bot Decks
description: How to use the web based decks built on the Streamer.bot website
published: true
date: 2022-08-04T16:48:13.175Z
tags: integrations, streamerbot, decks, website
editor: markdown
dateCreated: 2022-06-01T14:35:51.843Z
---

## Description
The streamer.bot website offers a "streamer deck" interface utilizing HTML that can be run on any device. Local and remote connections are available so that your mods can help you stream.

## Requirements
- Log in to https://streamer.bot
- Ensure the `Streamer.bot Connection` option is enabled in your user settings (it should be enabled by default)
  ![wiki1.png](https://cdn.discordapp.com/attachments/734080487009681490/981539873787875379/wiki1.png =800x)

- Enable the `Streamer.bot Website` integration in Streamer.bot
![bot-integration.png](https://cdn.discordapp.com/attachments/626215226261635082/981966838932074526/unknown.png =800x)

## Create a New Deck
Log in to the website in the top right and then click your icon to find "Decks"
![unknown.png](https://cdn.discordapp.com/attachments/848709180658941972/981543274152071218/unknown.png =800x)

Click on the "New Deck" button to generate a fresh deck.
![unknown-deck.png](https://cdn.discordapp.com/attachments/848709180658941972/981545649952686140/unknown.png =800x)
![freshdeck.png](https://cdn.discordapp.com/attachments/734080487009681490/981550483334393886/unknown.png =800x)
![deckpageoptions](https://cdn.discordapp.com/attachments/734080487009681490/981550873404641320/unknown.png =800x)
At the top of the deck's page are 4 things of importance to note:
- The "Signal" icon that will allow you to try a reconnect if you need one
- The "Connection Toggle" icon that will allow you to switch from a remote to a local connection
- The "Gear" icon for this decks options like number of buttons, viewport size, and security 
- Launch Deck button to generate the deck's URL for use in any web browser

## Deck Options
The options popup allows for greater configuration and styling. It has 4 sections:
- General
- Scaling
- Styles
- Security

### General
![general-options](https://cdn.discordapp.com/attachments/734080487009681490/981552598031138886/unknown.png =800x)
General tab allows us to rename the deck as well as enable/disable remote connections and change IPs and port.

### Scaling
![scaling-options](https://cdn.discordapp.com/attachments/734080487009681490/981552803807895592/unknown.png =800x)
Scaling options allow for the number of button by changing the number of Rows and Columns. You can also adjust your viewport for size restrictions. Default is "Auto".

### Styles
![styles-options](https://cdn.discordapp.com/attachments/734080487009681490/981553099535695972/unknown.png =800x)
Styles tab allows for changing the background color of the overall deck and allow for custom padding and gaps between buttons.

### Security
![seceurity-options](https://cdn.discordapp.com/attachments/734080487009681490/981553115625054208/unknown.png =800x)
The Security option are for allowing public or private access to the deck. Setting a deck to private and entering a users discord name and number where it says "User Access" will restrict access to only those added and the broadcaster. Setting to private without any names added secures it to the broadcaster only. Public will allow anyone with the link to access the deck (until changed to Private or deleted).

> To add a user to a private deck, **the user being added must have previously logged onto the website using discord and then gone to the "Decks" page, at least once.** After they have done that you can paste the full Discord ID username#number (Lyfesaver#1974, VRFlad#0001 or GoWMan#6611 for example) then their name will appear in the dropdown to select it.
{.is-info}


> **Decks will continue to work after streaming has stopped if Streamer.bot is still running.**
{.is-warning}

## Create a Button
Each button can be styled with images, GIFs, background and text colors, icons as well as a drop down for selecting the action to associate with it. Arguments for the button can also be set.

![button-options](https://cdn.discordapp.com/attachments/734080487009681490/981563671861940274/unknown.png =800x)
Give the button a Name and choose an Action, at the minimum, to create a button. 
Alternatively, you can send arguments with the packet back to the bot when the button is pressed.
Click on the image to set a PNG, JPG or GIF
Give the button a background color and/or change the color of the text used for the button name.
Icons can be set using the icon name from https://icones.js.org

## Launch Your Deck
Clcik the "Launch Deck" button in the top right to open a new tab with your URL for the deck. This can be opened on another PC, phone, tablet or even docked into your OBS. If access allowed by other users or it's public, copy and paste the URL to share.

## Variables
The following arguments are sent with all button actions and will be available in your Streamer.bot instance as variables

| Variable | Description |
|      ---:|-------------|
| `streamerbotUserId` | Streamer.bot user ID |
| `streamerbotUserDiscordId` | The Discord user ID of the redeemer |
| `streamerbotUserUsername` | The Streamer.bot username of the redeemer e.g. DiscordUsername#0000 |

Any additional variables you have configured at the deck or button level will also be available in your Streamer.bot actions.
