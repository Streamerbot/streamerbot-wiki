---
title: Websocket Clients
description: 
published: true
date: 2022-04-16T18:05:05.321Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:37:08.368Z
---

Connect to other websocket servers and setup an action in [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code) to react to events that are emitted by the the server.  One example is to connect to the Data Puller Beat Saber mod and do various things depending on the data that is pushed out
***
**NOTE** Currently, due to the nature of the Websocket Client, the only real use for these is within the Execute C# code, sub-action will likely be created in due time.
***
Navigate to the `Websockets` tab within `CPH`, and then the `Clients` tab and you can add/edit/delete clients.

When adding a client, you need to provide the websocket address in the form of `ws://127.0.0.1:8080/`, you can also enabled Auto Connect on Startup, and Reconnect on Disconnect with a specified retry interval (in seconds).  In addition, you can provide actions for the `Connected`, `Disconnected` and `Message` events.

The `Message` event is the main one you're going to want to assign an action to.  The data is passed as a text data in the argument `%message%` which you can retrieve from the `args` variable within your C# code, and parse/act on it accordingly.

> Example: **DO NOT ACTUALLY USE THIS, IT WILL SPAM YOUR CHAT IF IT IS AN ACTIVE CLIENT**

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