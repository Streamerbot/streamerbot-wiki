---
title: General
description: C# Available Methods Reference
published: true
date: 2023-03-04T14:08:30.076Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:47:28.087Z
---

## General
```csharp
int Between(int min, int max);
```

```csharp
double NextDouble(); // get a random value between 0f and 1f
```

```csharp
void Wait(int milliseconds);
```

```csharp
string UrlEncode(string text);
```

```csharp
string EscapeString(string text);
```

## Source & Event Type

Use these methods to get the __source and the eventType.
```csharp
EventSource GetSource();
EventType GetEventType();
```

Examples:

```csharp
if (CPH.GetEventType() == EventType.YouTubeFirstWords) { ... }
```
```csharp
if (CPH.GetSource() == EventSource.Twitch) { ... }
```

To use this feature you need to add this to the top of the code.
```csharp
using Streamer.bot.Common.Events;
```

## Actions
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

```csharp
bool ActionExists(string actionName);
```

## Action Queues
```csharp
void PauseActionQueue(string name);
void PauseAllActionQueues();
```

```csharp
void ResumeActionQueue(string name, bool clear = false);
void ResumeAllActionQueues(bool clear = false);
```

## Sound
```csharp
void PlaySound(string fileName, float volume = 1.0f, bool finishBeforeContinuing = false);
```

```csharp
void PlaySoundFromFolder(string path, float volume = 1.0f, bool recursive = false, bool finishBeforeContinuing = false);
```

## Keyboard Press
```csharp
void KeyboardPress(string keyPress);
```

## C# Execute Method
```csharp
bool ExecuteMethod(string executeCode, string methodName);
```

## Logging
```csharp
void LogInfo(string logLine);
void LogWarn(string logLine);
void LogDebug(string logLine);
void LogVerbose(string logLine);
```

## Credits & First Words
```csharp
void AddToCredits(string section, string value, bool json = true)
```

```csharp
void ResetCredits();
void ResetFirstWords();
```

## Timers
```csharp
void DisableTimer(string timerName);
void EnableTimer(string timerName);
```

## Variables
set an argument to be used in subsequent sub-actions{.subtitle}

```csharp
void SetArgument(string variableName, object value);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}