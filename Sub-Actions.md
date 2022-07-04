---
title: Sub-Actions
description: Reference of all Streamer.bot Sub-Actions
published: true
date: 2022-07-04T01:36:12.644Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:29.815Z
---


# Twitch
* [Create Clip *Create a 30s Twitch! clip*](/Sub-Actions/Twitch/Create-Clip)
* [Create Stream Marker *Create a Twitch! stream marker*](/Sub-Actions/Twitch/Create-Stream-Marker)
* [Emote Only *Set Twitch! chat to emote only mode*](/en/Sub-Actions/Twitch/Emote-Only)
* [Get Follow Age Info for Target  *Populate arguments for time since a user followed the channel*  *Valid modes:`User` `From Input` `Variable`*](/Sub-Actions/Twitch/Get-Follow-Age)
* [Get User Info for Target  *Populate arguments for specified user information* *Valid modes:`User` `From Input` `Variable`*](/Sub-Actions/Twitch/Get-User-Info-for-Target)
* [Send Message To Channel  *Send a custom message to the channel as either `Broadcaster` or `Bot Account`*](/en/Sub-Actions/Twitch/Send-Message-To-Channel)
* [Set Channel Game *Change the current channel category*](/en/Sub-Actions/Twitch/Set-Channel-Game)
* [Set Channel Title *Change the current stream title* ](/Sub-Actions/Twitch/Set-Title)
* [Slow Mode *Set Twitch! chat to slow mode*](/en/Sub-Actions/Twitch/Slow-Mode)
* [Subscriber Only *Set Twitch! chat to subscriber only mode*](/en/Sub-Actions/Twitch/Subscriber-Only)
* [Timeout User *Timeout specified user for set time*](/Sub-Actions/Twitch/Timeout-User)
* [Run Commercial *Trigger an ad break* *v0.15+*](/Sub-Actions/Twitch/Run-Commercial)
{.links-list}

# Main
* [Comment *Add a comment for information or reference*](/Sub-Actions/Comment)
* [Delay *Delay the next sub-action*](/Sub-Actions/Delay)
* [Get Quote *Load a `Quote` from the database*](/Sub-Actions/Get-Quote)
* [Get Random Number *Generate a Random Number* *Populates the `randomNumber` variable*](/Sub-Actions/Get-Random-Number)
* [Keyboard Press *Simulate a keybaord button press*](/Sub-Actions/Keyboard-Press)
* [Perform Command *Execute a Windows program / File*](/Sub-Actions/Perform-Command)
* [Pick Color *Populate colour conversion arguments*](/Sub-Actions/Pick-Color) [Variables](/Variables#pick-color)
* [Set Timer State *Enable / Disable timed actions*](/Sub-Actions/Set-Timer-State)
{.links-list}


# Actions
* [Clear Action Queue *Clear pending actions from a queue*](/Sub-Actions/Clear-Action-Queue)
* [Get Action Group State  *Check Enabled state of all actions in a group*](/Sub-Actions/action-group-state)
* [Get Action State *Check Enabled state of an action*](/en/Sub-Actions/Get-Action-State)
* [Run Action *Execute another SB action*](/Sub-Actions/Do-Action)
* [Set Action Group State  *Enable / Disable all actions in a group*](/Sub-Actions/action-group-state)
* [Set Action Queue Pause State *Pause / Resume an action queue*](/en/Sub-Actions/Set-Action-Queue-Pause-State)
* [Set Action State *Enable / Disable an action*](/Sub-Actions/action-state)
{.links-list}

# C#
* [Execute C# Code *Define and Execute custom C# Code*](/Sub-Actions/Code/Execute-CSharp-Code)
* [Available Methods *Predefined SB C# Methods*](/Sub-Actions/Code/Execute-CSharp-Code/Available-Methods)
* [Execute C# Method *Execute a C# Method already defined in another action*](/Sub-Actions/Code/Execute-CSharp-Method)
{.links-list}

# Commands
* [Get Commands *Populate variables to list command groups* *v0.1.5+* ](/en/Sub-Actions/Commands/Get-Commands)
* [Set Command Group State *Enable / Disable all commands in a group*](/Sub-Actions/command-group-state)
* [Set Command State *Enable / Disable a single command*](/Sub-Actions/Get-Command-State)
* [Get Command Group State *Check Enabled state of all commands in a group* *UPDATE ME (combine with Set Command Group State)*](/Sub-Actions/command-group-state)
* [Get Command State *Check Enabled state of a single command* *CREATE ME (combine with Set Command State)*](/Sub-Actions/Get-Command-State)
{.links-list}

# [File](/en/Sub-Actions/File)
* [Read Lines from File *Read every line from a file into sequential arguments* *Populates `lineCount` & `line#` variables*](/Sub-Actions/File#read-rines-from-file)
* [Read Random Lines From File *Read a single random line from file into an argument* *Populates `randomLine#` variable*](/en/Sub-Actions/File#read-random-line-from-file)
* [Write To File *Save data to specified file*](/en/Sub-Actions/File#write-to-file)
{.links-list}

# [Logic](/en/Sub-Actions/Logic)

All logic in Streamer.bot must be performed against active `Arguments`. As any argument can only persist until the end of the running action if data need to be saved between actions, `Global Variables` can be used. Their data must be copied into an Argument to be usable

> Global Variables should be stored in `camelCase` ie. with the initial letter in lowercase. 
There is currently no error checking preventing upper case but the data will not be retrievable by sub-actions if you do 
{.is-danger}

> It is best practice to use different names for the `Global` and the `Argument`. 
Some functions have been known to fail when they are named the same
{.is-warning}

* [Global (Get) *Read data from a`Global Variable` into an argument*](/en/Sub-Actions/Logic/Global-Variables#global-get)
* [Global (Set) *Save data to a custom `Global Variable`*](/en/Sub-Actions/Logic/Global-Variables#global-set)
* [If/Else *Performs an `Action` if logical test is `True`*](/en/Sub-Actions/Logic/if-else)
* [Set Argument *Store / Manipulate data in an argument*](/Sub-Actions/Logic/Set-Argument)
* [Break *Diagnostic user only, cancels the running action*](/Sub-Actions/Logic/Break)
{.links-list}

# Network
* [Fetch URL *Retrieve data from a URL and populate into an argument*](/Sub-Actions/Network/Fetch-URL)
* [UDP Broadcast *Transmit custom data payload over UDP protocol*](/Sub-Actions/Network/UDP-Broadcast)
{.links-list}


# OBS
* [Flip Source *Inverts the source vertically*](/Sub-Actions/OBS/Flip-Source)
* [Get Current Scene *Populates the `currentScene` argument with the currently active scene name*](/Sub-Actions/OBS/Get-Current-Scene)
* [Get Scene Item Properties *Populates the `props.xyz` arguments*](/Sub-Actions/OBS/Get-Scene-Item-Properties)
* [Hide Group's Sources *Hide all sources within a specified OBS source group*](/Sub-Actions/OBS/Hide-Group's-Sources)
* [Hide Source's Filters *Hide all filters on a specified source*](/Sub-Actions/OBS/Hide-Source-Filters)
* [Raw *Execute custom OBS Websocket instructions*](/Sub-Actions/OBS/Raw)
* [Recording *Enable / Disable OBS recording state*](/Sub-Actions/OBS/Recording)
* [Rotate Source *Set source rotation translation*](/Sub-Actions/OBS/Rotate-Source)
* [Set Active Scene *Set actively broadcasting scene*](/Sub-Actions/OBS/Set-Active-Scene)
* [Set Browser Source URL *Set the URL of an OBS browser source*](/Sub-Actions/OBS/Set-Browser-Source-URL)
* [Set GDI Text *Change the text shown in a GDI+ source*](/Sub-Actions/OBS/Set-GDI-Text)
* [Set Image Source File *Set filepath for Image source* *v0.1.5+*{.version-badge} ](/Sub-Actions/OBS/Set-Image-Source-File)
* [Set Media Source File *Set filepath for Media source* *v0.1.5+*{.version-badge} *CREATE ME*](/Sub-Actions/OBS/Set-Media-Source-File)
* [Set Media State *Media playback controls for specified source* *`Play`,`Pause`,`Restart`,`Stop`,`Next`,`Previous`* *CREATE ME*](/Sub-Actons/OBS/Set-Media-State)
* [Set Random Group Source Visible *Set a random source in an OBS group to `Visible`* *Excludes sources already visible*](/Sub-Actions/OBS/Set-Random-Group-Source-Visible)
* [Set Replay Buffer State *Sets the state of the OBS Replay Buffer* *v0.1.5+*{.version-badge} *CREATE ME*](/Sub-Actions/OBS/Replay-Buffer-State)
* [Set Scene Filter State *Enable / Disable a scene filter* *CREATE ME*](/Sub-Actions/OBS/Scene-Filter-State)
* [Set Source Audio Track State *Enable / Disable an OBS audio track* *Requires obs-websocket 4.9.1*{.version-badge} *CREATE ME*](/Sub-Actions/OBS/Source-Audio-Track-State)
* [Set Source Filter State *Enable / Disable a source filter*](/Sub-Actions/OBS/Set-Source-Filter-State)
* [Set Source Mute State *Mute / Unmute a source* *UPDATE ME*](/Sub-Actions/OBS/Set-Source-Mute-State)
* [Set Source Visibility *Hide / Unhide a source*](/Sub-Actions/OBS/Set-Source-Visibility)
* [Set State of a Random Filter *Enable / Disable a random source filter* *CREATE ME*](/Sub-Actions/OBS/Source-Random-Filter-State)
* [Streaming *Start / Stop streaming state*](/Sub-Actions/OBS/Streaming)
* [Take Screenshot *Take a screenshot of a scene / source and save to file*](/Sub-Actions/OBS/Take-Screenshot)
{.links-list}

# PolyPop
> Available as of **Streamer.bot** *v0.1.8*{.version-badge} and higher
{.is-info}
* [Trigger Alert](/en/Sub-Actions/PolyPop/Trigger-Alert)
{.links-list}

# Rewards
* [Configure Reward *Enable / Disable one or more channel point rewards*](/Sub-Actions/Rewards/Configure-Reward)
* [Set Cost *Change the channel point cost of a reward*](/Sub-Actions/Rewards/Set-Cost)
* [Set Enabled State *Enable / Disable a channel point reward*](/Sub-Actions/Reward/Set-Enabled-State)
* [Set Global Cooldown *Set cooldown time for a channel point reward* *CREATE ME*](/Sub-Actions/Rewards/Set-Global-Cooldown)
* [Set Paused State *Pause / Unpause redemptions for a channel point reward*](/Sub-Actions/Rewards/Set-Paused-State)
* [Set Prompt *Set the prompt text shown for a channel point reward* *v0.1.5+*{.version-badge}](/Sub-Actions/Rewards/Set-Prompt)
* [Set Title *Set the name of a channel point reward* *v0.1.5+*{.version-badge}](/Sub-Actions/Rewards/Set-Title)
* [Update *Set `Title`,`Prompt`,`Cost` and `Cooldown` for a channel point reward in single sub-action* *v0.1.5+*{.version-badge}](/Sub-Actions/Rewards/Update)
* [Update Redemption Status *Mark the channel point redeem as `Completed` or `Rejected` (Rejecting will automatically refund points to the user)*](/Sub-Actions/Rewards/Redemption-Status)
{.links-list}

# Streamlabs Desktop
* [Flip Source *Inverts the source vertically*](/Sub-Actions/SLOBS/Flip-Source)
* [Get Current Scene *Populates the `currentScene` argument with the currently active scene name*](/Sub-Actions/SLOBS/Get-Current-Scene)
* [Hide Group's Sources *Hide all sources within a specified SLOBS source group*](/Sub-Actions/SLOBS/Hide-Groups-Sources)
* [Hide Source's Filters *Hide the filters on a source*](/Sub-Actions/OBS/Hide-Source-Filters)
* [Recording *Enable / Disable SLOBS recording state*](/Sub-Actions/SLOBS/Recording)
* [Rotate Source *Set source rotation translation*](/Sub-Actions/SLOBS/Rotate-Source)
* [Set Active Scene *Set actively broadcasting scene*](/Sub-Actions/SLOBS/Set-Active-Scene)
* [Set Browser Source URL *Set the URL of a browser source* *CREATE ME*](/Sub-Actions/SLOBS/Set-Browser-Source-URL)
* [Set GDI Text *Change the text shown in a GDI+ source*](/Sub-Actions/SLOBS/Set-GDI-Text)
* [Set Random Group Source Visible *Set a random source in an SLOBS group to `Visible`* *Excludes sources already visible*](/Sub-Actions/SLOBS/Set-Random-Group-Source-Visible)
* [Set Scene Filter State *Set visibility state of a scene filter* *CREATE ME*](/Sub-Actions/SLOBS/Scene-Filter-State)
* [Set Source Filter State *Enable / Disable a source filter*](/Sub-Actions/SLOBS/Set-Source-Filter-State)
* [Set Source Mute State *Mute / Unmute a source*](/Sub-Actions/SLOBS/Set-Source-Mute-State)
* [Set Source Visibility *Hide / Unhide a source*](/Sub-Actions/SLOBS/Set-Source-Visibility)
* [Set State of a Random Filter *Set visibility of a random source filter* *CREATE ME*](/Sub-Actions/SLOBS/Random-Filter-State)
* [Streaming *Start / Stop streaming state*](/Sub-Actions/SLOBS/Streaming)
{.links-list}

# Sounds
* [Play Sound *Play a specific sound file*](/Sub-Actions/Sounds#play-sound)
* [Play Sound From Folder *Play a random sound from a specified folder*](/en/Sub-Actions/Sounds#play-sounds-from-folder)
{.links-list}

# TwitchSpeaker
* [Speak *Send a custom message to be spoken to the TwitchSpeaker application* *v0.1.5+*{.version-badge} ](/Sub-Actions/TwitchSpeaker/Speak)
{.links-list}

# Voice Control
> Available as of **Streamer.bot** v0.1.8 and higher
{.is-info}
* [Set Voice Control Command *Trigger a command with your voice*](/en/Sub-Actions/Set-Voice-Control-Command)
* Set Voice Control Command State
{.links-list}

# VoiceMod
> Available as of **Streamer.bot** *v0.1.8*{.version-badge} and higher
{.is-info}
* [Get Current Voice *Queries VoiceMod for the current voice in use*](/en/Sub-Actions/VoiceMod/Get-Current-Voice)
* [Select Random Voice *Make Streamer.bot pick a random voice* ](/en/Sub-Actions/VoiceMod/Select-Random-Voice)
* [Select Voice *Select a Specific voice* ](/en/Sub-Actions/VoiceMod/Select-Voice)
* Select Voice by Id
* [Set Background Effect State *Toggle the Background Effects*](/en/Sub-Actions/VoiceMod/Set-Background-Effect-State)
* [Set Censor State *Toggle the Censor State*](/en/Sub-Actions/VoiceMod/Set-Censor-State)
* [Set Hear My Voice State *Toggles the hear my voice state*](/en/Sub-Actions/VoiceMod/Set-Hear-My-Voice-State)
* [Set Mute State *Toggles the mute state*](/en/Sub-Actions/VoiceMod/Set-Mute-State)
* [Set Voice Changer State *Toggles the Voice Changer state*](/en/Sub-Actions/VoiceMod/Set-Voice-Changer-State)
{.links-list}

# YouTube
> Available as of **Streamer.bot** *v0.1.8*{.version-badge} and higher
{.is-info}
* [Send Message To Channel *Send a messeage to your Youtube Channel*](/en/Sub-Actions/Youtube/Send-Message-To-YouTube)
* [Set Title *Set the title of your Youtube Stream*](/en/Sub-Actions/Youtube/Set-Title-YouTube)
* [Set Description *Set the Description of your Youtube Stream*](/en/Sub-Actions/Youtube/Set-Description-YouTube)
* [Set Title and Description *Set the Title and Description in One*](/en/Sub-Actions/Youtube/Set-Title-Description-YouTube)
{.links-list}