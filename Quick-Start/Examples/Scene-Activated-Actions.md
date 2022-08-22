---
title: Quick Start - Scene Activated Actions
description: Perform actions when changing scenes
published: false
date: 2022-08-18T12:57:03.008Z
tags: 
editor: markdown
dateCreated: 2022-08-07T18:26:07.707Z
---

> **Note:**
> This page uses *v0.1.11+*{.version-badge}
> If you are using *v0.1.0 - v0.1.10*{.version-badge} change  `%obsEvent.sceneName%` to `%obsEvent.scene-name%` and change the event `CurrentProgramSceneChanged` to `SwitchScenes`
> Updating is **highly** recommended
{.is-info}

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
What is shown above does if the scene name that is switched to equals the name 'Main' for example do the action 'Main' (you can change the action to your own name)

In the actions you can have a lot of things, in the tutorial the are some `Twitchspeaker` `->` `Speak` sub-actions but what also a lot of people do is

```csharp
if ("obsEvent.scene-name" Equals "Main") do "Enable Channel Points" then break"
if ("obsEvent.scene-name" Equals "BRB") do "Disable Channel Points" then break"
```
This `disable`/`enable` channel points you can check [this](/en/Quick-Start/Examples/Disable-Enable-Channel-Points)

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