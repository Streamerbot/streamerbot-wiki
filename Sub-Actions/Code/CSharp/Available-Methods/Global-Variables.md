---
title: Global Variables
description: C# Available Methods Reference
published: true
date: 2023-01-03T00:14:33.504Z
tags: 
editor: markdown
dateCreated: 2023-01-03T00:13:01.336Z
---

## General
```csharp
T GetGlobalVar<T>(string varName, bool persisted = true);
T GetUserVar<T>(string userName, string varName, bool persisted = true);
```

```csharp
void SetGlobalVar(string varName, object value, bool persisted = true);
void SetUserVar(string userName, string varName, object value, bool persisted = true);
```

```csharp
void UnsetGlobalVar(string varName, bool persisted = true);
void UnsetUserVar(string userName, string varName, bool persisted = true);
void UnsetUser(string userName, bool persisted = true);
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

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}