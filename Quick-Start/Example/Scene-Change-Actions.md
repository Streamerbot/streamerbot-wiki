---
title: Quick Start - Scene Activated Actions Example
description: Perform actions when changing scenes
published: false
date: 2022-08-08T20:31:17.705Z
tags: 
editor: markdown
dateCreated: 2022-08-07T18:26:07.707Z
---

> Finish later
{.is-danger}

## Guide

For this to work you need to use the OBS event `SwitchScenes`
![obs-event-tab-switchscenes.jpg](/quick-start/scene-activated-actions-example/obs-event-tab-switchscenes.jpg)
![obs-event-tab-switchscenes-zoomed.jpg](/quick-start/scene-activated-actions-example/obs-event-tab-switchscenes-zoomed.jpg)
And hook it up to an action in this case `Example 1`
You can do this with 2 ways

### Solutions
<details>
<summary>Solution 1</summary>
  
The way that most people use (what is shown in the [Daan - Tutorial](#daan-tutorials)'s tutorial)
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
![Thumbnail](https://i.ytimg.com/vi_webp/9ZuO3KrbvRw/maxresdefault.webp =60%x)

</details>
<details>
<summary>Solution 2</summary>
</details>

## Video Tutorial
### TerrierDarts
<div class=“iframe-container”><iframe src="https://www.youtube.com/embed/9Gx7b46y0S8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen" allow fullscreen style="border: none; max-width: 50%; width: 50%; aspect-ratio: 16/9;"></iframe></div>

### Daan - Tutorials
<div class=“iframe-container”><iframe src="https://www.youtube.com/embed/9ZuO3KrbvRw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen" allow fullscreen style="border: none; max-width: 50%; width: 50%; aspect-ratio: 16/9;"></iframe></div>