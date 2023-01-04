---
title: Commands
description: C# Available Methods Reference
published: true
date: 2023-01-04T02:49:39.966Z
tags: 
editor: markdown
dateCreated: 2023-01-04T02:49:39.966Z
---

## Enable/Disable Commands
```csharp
void EnableCommand(string id);
void DisableCommand(string id);
```

## Set Commands Cooldowns
```csharp
void CommandSetGlobalCooldownDuration(string id, int seconds);
void CommandSetUserCooldownDuration(string id, int seconds);
```

## Add to Commands Cooldowns
```csharp
void CommandAddToGlobalCooldown(string id, int seconds);
void CommandAddToUserCooldown(string id, int userId, int seconds);
void CommandAddToAllUserCooldowns(string id, int seconds);
```

## Reset Commands Cooldowns
```csharp
void CommandResetGlobalCooldown(string id);
void CommandResetUserCooldown(string id, int userId);
void CommandResetAllUserCooldowns(string id);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}