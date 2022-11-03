---
title: YouTube
description: C# Available Methods Reference
published: true
date: 2022-11-03T08:45:36.526Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:53:53.607Z
---

## Chat Message
```csharp
void SendYouTubeMessage(string message);
```

## User Variables
```csharp
T GetYouTubeUserVar<T>(string userName, string varName, bool persisted = true);
void SetYouTubeUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetYouTubeUserVar(string userName, string varName, bool persisted = true);
void UnsetYouTubeUser(string userName, bool persisted = true);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}