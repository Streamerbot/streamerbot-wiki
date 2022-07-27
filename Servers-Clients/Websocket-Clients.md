---
title: WebSocket Clients
description: Configure Streamer.bot to connect to an external WebSocket server
published: true
date: 2022-07-27T21:11:35.931Z
tags: websocket
editor: markdown
dateCreated: 2021-08-25T21:37:08.368Z
---

> **NOTE** 
> Currently, due to the nature of the Websocket Client, the only real use for these is within the [Execute C# Code](/en/Sub-Actions/Code/Execute-CSharp-Code) sub-action.
{.is-info}

# Overview

WebSocket clients allow you to connect to external WebSocket servers and setup corresponding actions using the [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) sub-action to react to events that are emitted by the the respective server.  

For example, you could connect to the **Data Puller Beat Saber Mod** and perform various actions based on the data receieved.


# Configuration

Navigate to the `Websockets` tab within `Streamer.bot`, and then the `Clients` tab and you can add/edit/delete clients.

When adding a client, you need to provide the websocket address in the form of `ws://127.0.0.1:8080/`, you can also enabled Auto Connect on Startup, and Reconnect on Disconnect with a specified retry interval (in seconds).  In addition, you can provide actions for the `Connected`, `Disconnected` and `Message` events.

The `Message` event is the main one you're going to want to assign an action to.  The data is passed as a text data in the argument `%message%` which you can retrieve from the `args` variable within your C# code, and parse/act on it accordingly.


# Example

> **WARNING**
> *DO NOT ACTUALLY USE THIS EXAMPLE, IT WILL SPAM YOUR CHAT IF IT IS AN ACTIVE CLIENT*
{.is-warning}

```csharp
using System;
using Newtonsoft.Json.Linq;

public class CPHInline
{
    public bool Execute()
    {
        var msg = args["message"].ToString();

        CPH.SendMessage(msg);

        // parse it to a json object if it was expected json
        var json = JObject.Parse(msg); 

        return true;
    }
}
```