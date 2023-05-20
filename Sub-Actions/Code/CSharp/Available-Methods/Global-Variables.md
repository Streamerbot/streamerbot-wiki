---
title: Global Variables
description: C# Available Methods Reference
published: true
date: 2023-01-27T16:57:12.173Z
tags: 
editor: markdown
dateCreated: 2023-01-03T00:13:01.336Z
---

## General
```csharp
T GetGlobalVar<T>(string varName, bool persisted = true);
void SetGlobalVar(string varName, object value, bool persisted = true);
void UnsetGlobalVar(string varName, bool persisted = true);
```

## Twitch
```csharp
T GetTwitchUserVar<T>(string userName, string varName, bool persisted = true);
void SetTwitchUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetTwitchUserVar(string userName, string varName, bool persisted = true);
void UnsetTwitchUser(string userName, bool persisted = true);
```

## YouTube
```csharp
T GetYouTubeUserVar<T>(string userName, string varName, bool persisted = true);
void SetYouTubeUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetYouTubeUserVar(string userName, string varName, bool persisted = true);
void UnsetYouTubeUser(string userName, bool persisted = true);
```

## Deprecated Methods
> **Deprecated**
> These methods will either be removed in a future version of **Streamer.bot**, it's best to move to the replacements, or no longer exist.
{.is-danger}

### User Vars

The following methods have counterparts in the Twitch and YouTube section
```csharp
T GetUserVar<T>(string userName, string varName, bool persisted = true);
void SetUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetUserVar(string userName, string varName, bool persisted = true);
void UnsetUser(string userName, bool persisted = true);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}