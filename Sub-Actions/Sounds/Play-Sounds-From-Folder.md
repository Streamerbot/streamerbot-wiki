---
title: Play Sound From Folder
description: 
published: true
date: 2021-11-26T00:29:00.265Z
tags: sounds, folder, recursive
editor: markdown
dateCreated: 2021-11-22T01:08:16.939Z
---

# Play Sound from Folder

This sub action allows you to play a sound file from a folder on your computer that is in the folder you specify in the dialog box. 

![sound_from_folder.png](/sound_from_folder.png)

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
