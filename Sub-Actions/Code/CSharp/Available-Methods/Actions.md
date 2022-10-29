---
title: Actions
description: C# Available Methods Reference
published: true
date: 2022-10-29T20:47:28.087Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:47:28.087Z
---

## General
```csharp
bool RunAction(string actionName, bool runImmediately = true);
```

```csharp
bool RunActionById(string actionId, bool runImmediately = true);
```

```csharp
void DisableAction(string actionName);
void EnableAction(string actionName);
``` 

> Requires minimum version v0.1.14
{.is-info}
```csharp
bool ActionExists(string actionName);
```
## Action Queues
```csharp
void PauseActionQueue(string name);
void PauseAllActionQueues();
void ResumeActionQueue(string name, bool clear = false);
void ResumeAllActionQueues(bool clear = false);
```

## UDP Broadcast
```csharp
int BroadcastUdp(int port, object data);
```

## Sound
```csharp
void PlaySound(string fileName, float volume = 1.0f, bool finishBeforeContinuing = false);
void PlaySoundFromFolder(string path, float volume = 1.0f, bool recursive = false, bool finishBeforeContinuing = false);
```

## TwitchSpeaker
```csharp
int TtsSpeak(string voiceAlias, string message, bool badWordFilter = false);
```

## Keyboard Press
```csharp
void KeyboardPress(string keyPress);
```

## C# Execute Method
```csharp
bool ExecuteMethod(string executeCode, string methodName);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}