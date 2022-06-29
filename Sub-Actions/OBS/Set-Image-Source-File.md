---
title: Set Image Source
description: Have streamer bot change the image source file path from a directory of choice 
published: true
date: 2022-05-17T21:29:24.471Z
tags: twitch, obs, youtube, image
editor: markdown
dateCreated: 2022-05-17T00:21:00.986Z
---

## Set Image Source 

This sub action allows you to set up streamer bot to load in an image from a file path that you specify. 


#### Pre-requirements
1.  OBS open and Streamer.bot connected 
2.  Image source in a set scene 
3.  The image you want Streamer.bot to load into the image source 

![obs_1_.png](/set-image-source/obs_1_.png){.align-center}


### Setup 

![capture.png](/set-image-source/capture.png){.align-center}

To do this all you need to do is open Streamer.Bot and select the action you would like to add this sub action to. Next in the Sub-Actions window right click a menu will appear. In this menu navigate through the following `Add Action` then `OBS` then in this menu click `Set Image Source File`


Next, A dialog box will appear now make sure that both OBS and Streamer bot are Running and connected to each other. 

![obs_image_source_dialog.png](/set-image-source/obs_image_source_dialog.png){.align-center}

Complete the fields in the box. Connection will be to the OBS Instance of your choice, if you connected to your OBS it will display a drop down of the scene available through the connection. Source you would need to select the (named image source). then for the file name click the `...` button on the file browser window and navigate to the image file you would like to load to that source. 

That’s it click the `Test` button to see if it works and the image should appear in your OBS preview.  When your happy click ok and you’re done.  



