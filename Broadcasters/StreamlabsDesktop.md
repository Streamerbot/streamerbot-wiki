---
title: Streamlabs Desktop
description: 
published: true
date: 2022-07-08T11:21:23.654Z
tags: broadcasters, streamlabsdesktop
editor: markdown
dateCreated: 2021-08-25T21:32:18.787Z
---

![streamlabs-logo.png](/logos/streamlabs-logo.png){.align-abstopright}
# Overview
> New with v0.0.50, Streamerbot can now control your instances of Streamlabs Desktop!
{.is-success}

Configuration page for one or more connection(s) to Streamlabs Desktop instance(s)

Adding at least one connection will allow you to control your OBS either through the various [sub-actions](/Sub-Actions#main) that have been included, or via the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) sub-action

# Guide
`Right-Click` -> `Add` to define a new connection
Give it a name and set the IP address and Port number of your SLOBS / Streamlabs Desktop installation

The Default values of `127.0.0.1` and `59650` will look for the out-of-box configuration for SLOBS / Streamlabs Desktop installed on the same computer as Streamerbot is running

`Token` is required and can be obtained through the settings page for SLOBS / Streamlabs Desktop

![SLOBS settings](/122339880-810b0280-cf39-11eb-9453-f6e4e6473f1e.png)

### Token

In SLOBS / Streamlabs Desktop settings go to **Remote Control**

Click to reveal the QR code and then click **Show Details**

You can now copy the `API Token` into the Streamer.Bot connection window

***

Connections can be configured to `Auto Connect on Startup`, and to `Reconnect on Disconnect` with a retry interval you specify in seconds

***

Once configured, connected SLOBS / Streamlabs Desktop sessions will report their status on this screen

![SLOBS connection](/122341198-1fe42e80-cf3b-11eb-9c5e-42217878766d.png)

### Current Scene

Shows the name of the currently broadcasting scene on that connection

### Stream Status

Shows the status of current streaming and recording activity

### Sources

Lists all sources present on the currently selected scene
