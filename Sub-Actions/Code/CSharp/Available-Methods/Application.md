---
title: Application
description: C# Available Methods Reference
published: false
date: 2022-10-29T20:37:54.811Z
tags: 
editor: markdown
dateCreated: 2022-10-28T17:10:24.521Z
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

## Logging
```csharp
void LogInfo(string logLine);
void LogWarn(string logLine);
void LogDebug(string logLine);
```

> Requires minimum version 0.1.14
{.is-info}

```csharp
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