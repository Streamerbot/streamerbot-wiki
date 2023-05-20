---
title: OBS Studio Events Guide
description: OBS Studio Events Reference (v5)
published: true
date: 2023-03-16T12:02:38.718Z
tags: 
editor: markdown
dateCreated: 2023-01-09T05:58:54.811Z
---

## Overview
OBS Studio events let you trigger actions on things that change in OBS, some of these events even have variables so you can see what's changed.

## Configuration
![overview](/broadcasters/obs/overview.png =500x)
![add obs event currentprogramscenechanged](/broadcasters/obs/add-obs-event-currentprogramscenechanged.png =500x)

To use an event you need to go to the `Stream Apps --> OBS` tab and add and an event (<kbd>right-click</kbd> at the bottom of this page, where it says `Event`). Now fill out the data so choose an event out of the list for this example `CurrentProgramSceneChanged` and choose an action, now with this example when you change scenes the selected action will trigger and it will give [these variables](/Broadcasters/OBS/Events/Scene-Events/CurrentProgramSceneChanged#variables) this can be used for a ton of things e.g. for an if statement as shown on the page or for a send message to channel sub-action with: `%obsEvent.sceneName%`. But it can be used for more like for the [StreamStateChanged](/Broadcasters/OBS/Events/Output-Events/StreamStateChanged) event, this most oftenly used with if statements as shown on the page, simply just add them in the selected action and it all works.

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
{.btn-grid my-5}