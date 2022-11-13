---
title: General
description: C# Available Methods Reference
published: true
date: 2022-11-13T23:42:25.308Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:47:28.087Z
---

## General
```csharp
int Between(int min, int max);
double NextDouble(); // get a random value between 0f and 1f
```

```csharp
void Wait(int milliseconds);
```

```csharp
string UrlEncode(string text);
string EscapeString(string text);
```

```csharp
EventSource GetSource();
EventType GetEventType();
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

> Requires minimum version 0.1.14
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

## Sound
```csharp
void PlaySound(string fileName, float volume = 1.0f, bool finishBeforeContinuing = false);
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

// Added in v0.1.14
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
```csharp
void SetArgument(string variableName, object value); // set an argument to be used in subsequent sub-actions
```

## Global Variables
```csharp
T GetGlobalVar<T>(string varName, bool persisted = true);
void SetGlobalVar(string varName, object value, bool persisted = true);
void UnsetGlobalVar(string varName, bool persisted = true);
T GetUserVar<T>(string userName, string varName, bool persisted = true);
void SetUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetUserVar(string userName, string varName, bool persisted = true);
void UnsetUser(string userName, bool persisted = true);
```

## Groups
```csharp
bool UserInGroup(int userId, string groupName);
bool UserInGroup(string userName, string groupName);
bool AddUserToGroup(int userId, string groupName);
bool AddUserToGroup(string userName, string groupName);
bool RemoveUserFromGroup(int userId, string groupName);
bool RemoveUserFromGroup(string userName, string groupName);
```

## Commands
### Enable/Disable Commands
```csharp
void EnableCommand(string id);
void DisableCommand(string id);
```

### Set Commands Cooldowns
```csharp
void CommandSetGlobalCooldownDuration(string id, int seconds);
void CommandSetUserCooldownDuration(string id, int seconds);
```

### Add to Commands Cooldowns
```csharp
void CommandAddToGlobalCooldown(string id, int seconds);
void CommandAddToUserCooldown(string id, int userId, int seconds);
void CommandAddToAllUserCooldowns(string id, int seconds);
```

### Reset Commands Cooldowns
```csharp
void CommandResetGlobalCooldown(string id);
void CommandResetUserCooldown(string id, int userId);
void CommandResetAllUserCooldowns(string id);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}