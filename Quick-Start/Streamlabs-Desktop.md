---
title: Quick Start - Streamlabs Desktop
description: Set up Streamer.bot to remotely control your Streamlabs Desktop instance
published: true
date: 2022-08-04T15:57:58.969Z
tags: 
editor: markdown
dateCreated: 2022-08-04T13:56:19.296Z
---

## Prerequisites

Obtain your **API Token** and **Port** from your Streamlabs Desktop settings.

![WebsocketSettings](https://contenthub-cdn.streamlabs.com/static/imgs/mceclip2-360005539093.png =500x)

Later, you will need to match these settings in Streamer.bot

## Configuration

Streamlabs Desktop configuration can be found by navigating to the following tabs in Streamer.bot:
`Broadcasters` -> `Streamlabs Desktop`

![streamlabs_desktop_landing_page.png](/quick-start/streamlabs_desktop_landing_page.png =700x)

To add a new connection, <kbd>Right-Click</kbd> -> <kbd>Add</kbd> to open the new connection dialogue.

![streamlabs_desktop_connection_popup.png](/quick-start/streamlabs_desktop_connection_popup.png)

Configuration options are outlined below:

### Name
Enter any name or description for this Streamlabs Desktop connection

### Host
Enter the local IP address of your Streamlabs Desktop instance
The default value of `127.0.0.1` will find instances on the same PC

### Port
Enter the **port** found in Streamlabs Desktop settings earlier
The default value is `59650`

### Token
Enter the **API Token** value found in Streamlabs Desktop settings earlier

### Auto Connect on Startup
Enable this option to automatically connect to Streamlabs Desktop when you start Streamer.bot

### Reconnect on Disconnect
Enable this option to automatically reconnect to Streamlabs Desktop if the connection is lost

### Retry Interval
Amount of time, in seconds, to wait between each reconnection attempt

---

- [<i class="mdi mdi-chevron-left"></i> **Quick Start Guide *Go Back***](/en/Quick-Start)
- [<i class="mdi mdi-chat"></i> **Up Next *Configure basic chat commands***](/en/Quick-Start/Commands)
{.btn-grid .my-5}