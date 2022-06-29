---
title: Version 0.0.43
description: 
published: true
date: 2021-08-26T02:09:48.130Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:35:55.625Z
---

# Version 0.43

Jump to [New Features](#new-features)

* Execue code window is now resizeable
* Fix audio selection issues
* Add a simple online version check, uses a file in this repo to get the current version
* Add new sub-action Execute C# Method
* Fix websocket client auto-reconnect
* Ability to have a [KnownBots Group](https://github.com/nate1280/ChannelPointsHandler/wiki/Version-0.43#known-bots)
* New feature: [Credits](https://github.com/nate1280/ChannelPointsHandler/wiki/Version-0.43#credits)

**NOTE** This version will request a new permission, specifically reading editors on your channel, this is for the Credits feature

***
# New Features
## Execute C# Method
Using this sub-action, you can call into an existing execute code, and call another method.  If you have the Execute C# Code setup for `Keep Alive` and `Precompile on Startup` you can use `private` variables within the class to preserver data between calls.

The methods must be in the form of, a return type of `bool` with no parameters:
```csharp
public bool MethodName()
{
    // your code here
}
```

## KnownBots Group
If you create a group called `KnownBots`, and add users to this group, they will be excluded from the `%raiderNames%` variable that gets added during raids; this will likely be expanded upon for further usages.

## [Credits](https://github.com/nate1280/ChannelPointsHandler/wiki/Credits)
The script from SLCB has finally been brought over into CPH. It can be configured to include only certain events and information, and the resulting information can be retrieved by using a command on the websocket server.

This feature will likely be evolving, so consider this a first pass implementation to get something in place, it should be feature parity (and then some) with the script.  The only thing I believe that is missing are top gift subs, but I unfortunately do not track this information, and there is no way to get this from twitch that I can see.  Adding new features and capabilities to this is always posible.

The 2 new wbesocket server requests are `GetCredits` and `ClearCredits`.  There will be an example posted in the Nook on how to use/integrate this hopefully