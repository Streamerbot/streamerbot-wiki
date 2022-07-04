---
title: Hype Train
description: Twitch Hype Train Events
published: true
date: 2022-06-30T20:46:20.166Z
tags: twitch, hypetrain
editor: markdown
dateCreated: 2022-01-22T02:59:47.855Z
---

# Hype Train
In this tab you can assign actions to the various levels of the hype train. 

To get to this tab you need to click through the following tabs, First click the `Settings` tab next click on the `Events` tab then finally click the `Hype Train` tab. You should now see a window just like the image below.

![hypetrain.png](/hypetrain.png)

So in this Tab you can see 5 sections: Start, Progression, Level Up, and Finish. Each section will be explained below in their own sections. 

## Start

In this section you can set an action to trigger when a Hype Train is started in your Twitch channel. All you need to do is make sure you have an action created for this event and we will assign this action to the `Start` trigger event in this tab. To do this click the button `<No Action Selected>` now a window with all your actions will appear like the one below. 

![actionshype.png](/actionshype.png)

Select the relevant event in this case it would be the `Start Event Action` for this section.  Now this has been set when a hype train has started in your channel Streamer.bot will trigger the hype train start action. 

## Progression

In this section you can set an action to trigger when a Hype Train is progressing in your twitch channel. All you need to do is make sure you have an action created for this event and we will assign this action to the `Progression` trigger event in this tab. To do this click the button `<No Action Selected>` 

Select the relevant event in this case it would be the `Progression Action` for this section.  Now this has been set when a hype train progresses in your channel Streamer.bot will trigger this action. 


## Level Up 

In this section you can set an action to trigger when a Hype Train progresses through each of the levels. You can also add variation to each level that is triggered. To do this in the `Level Up` section you will need to add action to each level in the drop down menu or alternatively just assign an action to the default `Generic`. 

![hype_levels_.png](/hype_levels_.png)

To do this select an option from the drop down whether it's the generic or the level 1-5. Select one then click the button `<No Action Selected>` an action window will appear from here you would select the relevant action to the event in this case it would be the `A Level Up` for this section. Now this has been set when a hype train progresses in your channel Streamer.bot will trigger this action(s).

## Finish 

In this section you can set an action to trigger when a Hype Train has finished in your Twitch channel. All you need to do is make sure you have an action created for this event and we will assign this action to the `Finish` trigger event in this tab. To do this click the button `<No Action Selected>` now a window with all your actions will appear, select the action you want to run when this event is triggered.

## Test Section 

On the right in this tab is the test section where you can test all that you have just set up. You can test the events, level goal and level total these will let you test the variations and the progression actions you have. Total will let you test the finished event you have set.


# Variables


Variable | Description | Notes
---------:|------------|---
`level` | Current level | `(1-5)`
`percent` | percent complete of the level
`percentDecimal` | percent completion of the level as a decimal value
*`contributors` | Number of contributors in the hype train | Not available on `Hype Train Start`
`conductor` | Twitch User ID of the conductor



## Level Up

Variable | Description
---------:|------------
`prevLevel` | Previous level of the hype train | `(1-4)`

## Progression

Variable | Description
---------:|------------
`user` | The user who is contributing to the hype train

