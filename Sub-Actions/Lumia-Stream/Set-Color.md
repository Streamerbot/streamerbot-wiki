---
title: Set Color
description: Lumia Stream Sub-Action Reference
published: false
date: 2022-08-30T08:55:36.791Z
tags: v0.1.11, lumia stream, lights, color, brightness, smart home, automation
editor: markdown
dateCreated: 2022-08-25T21:54:15.039Z
---

## Overview
![streamer.bot-intergration-lumia-stream-sub-action-set-color-default.png](/intergrations/lumia-stream/sub-actions/set-color/streamer.bot-intergration-lumia-stream-sub-action-set-color-default.png)

## Configuration
> You can delete any off these fields and it will work, so for example if you don't want to change the brightness, remove the brightness field.
{.is-info}
#### Colour
A hex value used to change the colour of your light(s).

#### Brightness
A value that changes the brightness of your light(s).

#### Duration
A millisecond value used for a delay before switching back to default after the `Set Color` sub-action.

#### Transition
The time it takes to transition from your current light properties to the set color properties.

#### Skip Queue
This will skip the Lumia Stream `Queue` that's visible in your `Dashboard`.

#### Default
This will ignore the streamer.bot `Set Color` settings and use the default Lumia Stream settings.

#### Light
A list of all your lights that you've added with Lumia Stream. If you don't select any lights it will automatically use all your Lumia Stream configured lights.

---

- [<i class="mdi mdi-chevron-left"></i> **Lumia Stream *Go Back***](/en/Sub-Actions/Lumia-Stream)
{.btn-grid .my-5}