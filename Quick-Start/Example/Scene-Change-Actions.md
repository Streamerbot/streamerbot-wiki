---
title: Quick Start - Scene Activated Actions Example
description: Perform actions when changing scenes
published: false
date: 2022-08-08T22:30:46.725Z
tags: 
editor: markdown
dateCreated: 2022-08-07T18:26:07.707Z
---


## Navigation
* [Guide](#guide)
* [Solutions](#solutions)
  * [Solution 1 - UI if Statements](#solution-1-ui-if-statements)
  * [Solution 2 - C# Option](#solution-2-c-option)
* [Video Tutorials](#video-tutorials)
## Guide

For this to work you need to use the OBS event `SwitchScenes`

![obs-event-tab-switchscenes.jpg](/quick-start/scene-activated-actions-example/obs-event-tab-switchscenes.jpg =700x)
![obs-event-tab-switchscenes-zoomed.jpg](/quick-start/scene-activated-actions-example/obs-event-tab-switchscenes-zoomed.jpg =700x)

And hook it up to an action in this case `Example 1`
You can do this with 2 ways

## Solutions
### Solution 1 - UI if Statements

The way that most people use (what is shown in the [Daan - Tutorial](#video-tutorials)'s tutorial)
Is with `if statements`
![actions-tab-daantutorials-if-statements.jpg](/quick-start/scene-activated-actions-example/actions-tab-daantutorials-if-statements.jpg)
```csharp
if ("obsEvent.scene-name" Equals "Main") do "Main" then break"
if ("obsEvent.scene-name" Equals "Intermission") do "Intermission" then break"
if ("obsEvent.scene-name" Equals "Gaming") do "Gaming" then break"
```
In these if statements is shown:
```json
if the scene where you have changed to is named "Main" do the action "Main"
if the scene where you have changed to is named "Intermission" do the action "Intermission"
if the scene where you have changed to is named "Gaming" do the action "Gaming"
```
As shown in the thumbnail below you can for example hook it up like this
```text
Main == Light Red
Intermission == Light Green
Gaming == Light Blue
```
![Thumbnail](https://i.ytimg.com/vi_webp/9ZuO3KrbvRw/maxresdefault.webp =40%x)

---
### Solution 2 - C# Option

You Will need to create a new action, this is what will be tied to the OBS Event. I would go for something like `SceneSelection` You  will need to add 2 Sub-Actions to this action, 
```
OBS Get Current Scene
Execute Code (C#)
```
**This is the C# code you will need.**
```cs
using System;

public class CPHInline
{
	public bool Execute()
	{
		var scene = args["currentScene"].ToString();
		CPH.RunAction(scene);
		return true;
	}
}
```
Once this is set up Just start Creating New Actions that are named the same as your scene and then when ever that scene is active it will run the Action. Meaning When you go to your `Just Chatting` Scene it will run the action called `Just Chatting`. If no action exists nothing will happen.

## Video Tutorials

<section class="overview-grid my-5">
<div>

Daan - Tutorials{.overline}
  
<span></span>

<div class=“iframe-container”><iframe src="https://www.youtube.com/embed/9ZuO3KrbvRw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen" allow fullscreen style="border: none; max-width: 100%; width: 100%; aspect-ratio: 16/9;"></iframe></div>

</div>
  <div>

TerrierDarts{.overline}

<span></span>

<div class=“iframe-container”><iframe src="https://www.youtube.com/embed/9Gx7b46y0S8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen" allow fullscreen style="border: none; max-width: 100%; width: 100%; aspect-ratio: 16/9;"></iframe></div>

</div>
</section>