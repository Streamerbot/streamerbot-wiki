---
title: OBS
description: 
published: true
date: 2022-06-29T17:34:18.417Z
tags: integrations, obs
editor: markdown
dateCreated: 2021-08-25T21:32:10.502Z
---

![obs.svg](/logos/obs.svg){.align-abstopright}

# Overview
Configuration page for one or more connection(s) to OBS Studio instance(s)

> OBS Websocket v4.x is the only supported version at this time, v5.x requires a re-write and is being worked on
Download OBS Websocket plugin **4.9.1** [here](https://obsproject.com/forum/resources/obs-websocket-remote-control-obs-studio-from-websockets.466/)
{.is-warning}

Adding at least one connection will allow you to control your OBS either through the various [sub-actions](/Sub-Actions#main) that have been included, or via the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) sub-action

![broadcasters-obs-018.png](/broadcasters-obs-018.png)

> If you are using **0.1.7** or below the OBS configuration is found as a top level tab but the functionality is the same
{.is-info}


Once configured, connected OBS sessions will report their status on this screen

# Setup
`Right-Click` -> `Add` to define a new connection
Give it a name and set the IP address and Port number of the OBS Websocket

The Default values of `127.0.0.1` and `4444` will look for the out-of-box configuration for OBS installed on the same computer as CPH is running

`Password` Will not be required unless you have specified one in OBS

![New Connection](/119574587-9adb7e80-bdad-11eb-82c1-ec9ed668a40d.png)


Connections can be configured to `Auto Connect on Startup`, and to `Reconnect on Disconnect` with a retry interval you specify in seconds

***

### OBS Information

Shows the version number of OBS and the installed Websocket plugin

### Current Scene

Shows the name of the currently broadcasting scene on that connection

### Stream Status

Shows the status of current streaming and recording activity

### Sources

Lists all sources present on the currently selected scene

# Events

> OBS Events requires **Streamer.bot** version 0.1.4 or higher.
{.is-info}

You can assign actions to events that OBS transmits across the websocket connection.

The data that an event emits, is added onto the arguents the same way it is with results from `OBS Raw`, as well as a `%obsEvent._json%` variable that can be parsed in C# (`JObject.Parse()`) for easier use.

OBS events are per-connection based.

* [OBS Events *contains a list of events that are supported, this matches what the 4.9.x OBS websocket documentation lists.*](/en/Integrations/OBS/OBS-Events)
{.links-list}

# Requests
* [OBS Requests *Contains a list of requests that are supported with OBS raw.*](/en/Integrations/OBS/OBS-Requests) 
{.links-list}