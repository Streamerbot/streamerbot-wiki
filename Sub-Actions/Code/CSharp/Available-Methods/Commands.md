---
title: Commands
description: C# Available Methods Reference
published: true
date: 2023-01-27T02:37:57.771Z
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
void CommandAddToUserCooldown(string id, string userId, int seconds);
void CommandAddToAllUserCooldowns(string id, int seconds);
```

## Reset Commands Cooldowns
This makes it so if there is a cooldown of e.g. 60 seconds and when running this while it's e.g 30s in it will reset the cooldown back to 60s to wait for another trigger of the command. A common misunderstanding is that this will set the cooldown to 0, but it will not.{.subtitle}

```csharp
void CommandResetGlobalCooldown(string id);
void CommandResetUserCooldown(string id, string userId);
void CommandResetAllUserCooldowns(string id);
```

## Remove Command Cooldowns
This will remove any cooldowns on the command, effectively making the command useable again.
{.subtitle}

```csharp
void CommandRemoveGlobalCooldown(string id);
void CommandRemoveUserCooldown(string id, string userId);
void CommandRemoveAllUserCooldowns(string id);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}