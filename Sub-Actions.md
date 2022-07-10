---
title: Sub-Actions
description: Reference of all Streamer.bot Sub-Actions
published: true
date: 2022-07-10T18:52:05.210Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:29.815Z
---


## Platform
<section class="btn-grid my-5">
    
  [<i class="mdi mdi-twitch text--twitch"></i> **Twitch *Control your Twitch channel settings, send chat messages, create clips, and more!***](/en/Sub-Actions/Twitch)
  
  [<i class="mdi mdi-youtube text--youtube"></i>**YouTube *Control your YouTube channel title, description, and send chat messages***](/en/Sub-Actions/YouTube)
  
</section>
<section class="btn-grid my-5">
    
  [<i class="mdi mdi-twitch text--twitch"></i>**Rewards *Control every aspect of your Twitch Channel Point Rewards***](/en/Sub-Actions/Rewards)
  
</section>


## Broadcaster
<section class="btn-grid my-5">
    
  [<img src="https://streamer.bot/img/integrations/obs.svg"/>**OBS Studio *Control everything!***](/en/Sub-Actions/OBS)
  
  [<img src="https://streamer.bot/img/integrations/streamlabs.png"/>**Streamlabs Desktop *Control everything!***](/en/Sub-Actions/Streamlabs-Desktop)
  
  [<img src="https://streamer.bot/img/integrations/polypop.png"/>**PolyPop *Trigger alerts in PolyPop***](/en/Sub-Actions/PolyPop)
  
</section>


## General
<section class="btn-grid my-5">
    
  [<i class="mdi mdi-view-agenda primary--text"></i>**Main *Keystrokes, timers, delays, comments, and more...***](/en/Sub-Actions/Main)
  
  [<i class="mdi mdi-lightning-bolt primary--text"></i>**Actions *Modify Streamer.bot action state***](/en/Sub-Actions/Actions)
  
  [<i class="mdi mdi-code-braces primary--text"></i>**C# *Custom code actions***](/en/Sub-Actions/CSharp)
  
  [<i class="mdi mdi-comment-alert primary--text"></i>**Commands *Manage chat command state***](/en/Sub-Actions/CSharp)
  
  [<i class="mdi mdi-file-code primary--text"></i>**File *Read &amp; write from local files***](/en/Sub-Actions/File)
  
  [<i class="mdi mdi-state-machine primary--text"></i>**Logic *Manage variables, If/Else, Break***](/en/Sub-Actions/Logic)
  
  [<i class="mdi mdi-network primary--text"></i>**Network *Fetch URL, UDP Broadcast***](/en/Sub-Actions/Network)
  
  [<i class="mdi mdi-volume-high primary--text"></i>**Sounds *Play sound files***](/en/Sub-Actions/Sounds)
  
  [<i class="mdi mdi-account-voice primary--text"></i>**Voice Control *Manage Voice Control commands***](/en/Sub-Actions/Voice-Control)
  
</section>


## Integration
<section class="btn-grid my-5">
  
  [<i class="mdi mdi-speaker text--twitch"></i>**TwitchSpeaker *Send text to TwitchSpeaker TTS***](/en/Sub-Actions/TwitchSpeaker)
  
  [<img src="/logos/voicemod.png"/>**VoiceMod *Select voices, modify state, get current state***](/en/Sub-Actions/Logic)
  
</section>


# Main
* [Comment *Add a comment for information or reference*](/Sub-Actions/Comment)
* [Delay *Delay the next sub-action*](/Sub-Actions/Delay)
* [Get Quote *Load a `Quote` from the database*](/Sub-Actions/Get-Quote)
* [Get Random Number *Generate a Random Number* *Populates the `randomNumber` variable*](/Sub-Actions/Get-Random-Number)
* [Keyboard Press *Simulate a keybaord button press*](/Sub-Actions/Keyboard-Press)
* [Perform Command *Execute a Windows program / File*](/Sub-Actions/Perform-Command)
* [Pick Color *Populate colour conversion arguments*](/Sub-Actions/Pick-Color) [ - Variables](/Variables#pick-color)
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
* [Set Voice Control Command State *Set the Voice Control Command State*](/en/Sub-Actions/Set-Voice-Control-Command-State)
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
