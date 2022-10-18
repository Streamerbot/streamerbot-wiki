---
title: Sounds Sub-Actions
description: Play sound files directly from the Streamer.bot application
published: true
date: 2022-10-18T00:26:42.821Z
tags: 
editor: markdown
dateCreated: 2022-01-23T22:36:07.705Z
---

* [<i class="mdi mdi-volume-high primary--text"></i>**Play Sound *Play a sound file on your computer***](/en/Sub-Actions/Sounds/Play-Sound)
* [<i class="mdi mdi-volume-high primary--text"></i>**Play Sound From Folder *Play a sound file from a folder***](/en/Sub-Actions/Sounds/Play-Sounds-From-Folder)
{.btn-grid .my-5}

Streamer.bot has the capability of playing sounds directly from the application, no sources in your streaming software are required.

> Currently there is no way to pause or stop a sound once it has started other than forcing the application to close
{.is-warning}

You can choose a specific sound file to play or specify a folder and have the bot pick one at random

# Play Sound

Play a sound file on your computer.

![sub-action-sounds-play-sound-001.png](/sub-action-sounds-play-sound-001.png)

## Audio Device
Pick the audio device the sound should be played through.

Application default will use whatever audio device is configured in the application settings.

## Sound file to play
The sound file you would like to play.  Supported audio formats are, `mp3`, `wav`, `m4a` and `ogg`

## Finish playing before continuing
Enabling this will wait for the duration of the sound file before continuing onto the next action.  If this is disabled, the sound will start being played and immediately carry onto the next sub-action.

## Volume
Adjust the volume of the sound file.  This is a very basic volume adjustment, and is usually better to adjust the volume with a tool like Audacity.

---

# Play Sound from Folder

Play a sound file from a folder on your computer that is in the folder you specify in the dialog box. 

![sound_from_folder.png](/sound_from_folder.png)

> The `Test` button does not play the selected file, but picks a random sound to play from those available
{.is-info}


## Audio Device
Pick the audio device the sound should be played through.

Application default will use whatever audio device is configured in the application settings.

## Sound file to play
The sound file you would like to play.  Supported audio formats are, `mp3`, `wav`, `m4a` and `ogg`

## Finish playing before continuing
Enabling this will wait for the duration of the sound file before continuing onto the next action.  If this is disabled, the sound will start being played and immediately carry onto the next sub-action.

## Recursive
With this enabled, the bot will select from audio files not only in the selected directory, but in all sub-directories within that selected original one.  

Example: In the image below you can see the `<sub directory>\filename.mp3` of where the bot found the audio file within the original directory and sub directories.

![recursive.png](/recursive.png)

## Volume
Adjust the volume of the sound file.  This is a very basic volume adjustment, and is usually better to adjust the volume with a tool like Audacity.

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/en/Sub-Actions)  
- [<i class="mdi mdi-account-voice primary--text"></i> **Voice Control *Sub-actions reference for managing Voice Control commands***](/en/Sub-Actions/Voice-Control)
{.btn-grid .my-5}
