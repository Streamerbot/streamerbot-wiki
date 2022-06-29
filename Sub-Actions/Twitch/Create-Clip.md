---
title: Create Clip
description: 
published: true
date: 2022-06-06T02:14:28.777Z
tags: 
editor: markdown
dateCreated: 2021-11-02T04:15:59.794Z
---

# Create Clip

Streamer bot can create a 30 second clip.

There is no user configuration as regards to the title of the clip as this sub-action, and the underlying API call it makes to Twitch is basic. Because of this nature by default, it creates a 30 second clip, and the title is set to your current stream title.

To alter any of this, you would have to go back and edit the clip afterwards.

To have Streamer Bot do this all you need to do will be detailed here.

Select an action or create one just like in this screenshot below. In the sub-action pane right click then select `Add Sub-Action` next navigate down to `Twitch` then click `Create Clip` this will now create a sub-action called create clip.

![image.png](/create-clip/image.png){.align-center}

Example use of this could be to tie this action to a clip command so your mobile users can clip your streams right from chat in the twitch app. 