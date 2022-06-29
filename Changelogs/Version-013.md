---
title: Version 0.1.3
description: 
published: true
date: 2021-08-26T13:35:24.721Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:52.549Z
---

# Streamer.bot v0.1.3

## Some fixes/changes

* Fix logic if sub-action for does exist, code path was unreachable
* Fix importing actions which contained obs actions, was not correctly defaulting to first configured obs instance
* Fix importing actions which contained ClearActionQueue and SetActionQueuePauseState
* Fix ClearActionQueue and SetActionQueuePauseState to handle if an invalid queue has been selected
* Fix Pyramids, a change to the way emotes were handled broke this feature
* Twitch -> Configure Rewards, window is now resizeable and added a context menu for moving rewards as well
* Mask the Streamlabs and StreamElements tokens, with a show/hide button