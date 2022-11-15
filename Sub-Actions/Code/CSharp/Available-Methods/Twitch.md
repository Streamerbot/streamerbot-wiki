---
title: Twitch
description: C# Available Methods Reference
published: true
date: 2022-11-15T00:19:09.855Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:51:36.923Z
---

## General
```csharp
void SendMessage(string message, bool bot = true);
void SendAction(string action, bool bot = true);
```

```csharp
List<Cheermote> GetCheermotes();
```

```csharp
void TwitchSubscriberOnly(bool enabled = true);
void TwitchEmoteOnly(bool enabled = true);
```

> Changed `void` to `bool` in v0.1.14
{.is-info}
```csharp
bool SendWhisper(string userName, string message);
```

## Moderator
> Requires minimum version v0.1.14
{.is-info}
```csharp
bool TwitchAddModerator(string userName);
bool TwitchRemoveModerator(string userName);
```

## Vip
> Requires minimum version v0.1.14
{.is-info}
```csharp
bool TwitchAddVip(string userName);
bool TwitchRemoveVip(string userName);
```

## Messages
> Requires minimum version v0.1.14
{.is-info}

```csharp
bool TwitchClearChatMessages(bool bot = true);
bool TwitchDeleteChatMessage(string messageId, bool bot = true);
```

## Timouts / Bans
> Requires minimum version v0.1.14
{.is-info}

```csharp
bool TwitchBanUser(string userName, string reason = null, bool bot = false);
bool TwitchUnbanUser(string userName, bool bot = false);
```

```csharp
void TimeoutUser(string userName, int duration);
```

## Channel Rewards
```csharp
void DisableReward(string rewardId);
void EnableReward(string rewardId);
void PauseReward(string rewardId);
void UnPauseReward(string rewardId);
```

```csharp
void UpdateRewardCost(string rewardId, int cost, bool additive = false);
void UpdateRewardCooldown(string rewardId, int cooldown, bool additive = false);
```

```csharp
bool TwitchRedemptionFulfill(string rewardId, string redemptionId);
bool TwitchRedemptionCancel(string rewardId, string redemptionId);
```

```csharp
bool UpdateRewardTitle(string rewardId, string title);
bool UpdateRewardPrompt(string rewardId, string prompt);
bool UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null);
```

## Polls
```csharp
bool TwitchPollCreate(string title, List<string> choices, int duration, int channelPointsPerVote = 0);
void TwitchPollTerminate(string pollId);
void TwitchPollArchive(string pollId);
```

## Predictions
```csharp
string TwitchPredictionCreate(string title, List<string> options, int duration);
void TwitchPredictionCancel(string predictionId);
void TwitchPredictionLock(string predictionId);
void TwitchPredictionResolve(string predictionId, string winningId);
```

## Clips
> All clip data is returned as oldest to newest, this is a limitation of the Twitch API.  To get most recent clips, one would have to get all the clips for the user, one got-ya for this, there is a hard limit of 1000 clips that can be returned
{.is-info}

```csharp
List<ClipData> GetAllClips();
List<ClipData> GetClipsForGame(int gameId);
List<ClipData> GetClipsForUser(int userId);
List<ClipData> GetClipsForUser(string username);
```

```csharp
ClipData CreateClip();
```

```csharp
List<ClipData> GetClipsForUser(int userId, int count);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration, int count);
List<ClipData> GetClipsForUser(string userName, int count);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(string username, TimeSpan duration);
List<ClipData> GetClipsForUser(string username, TimeSpan duration, int count);
List<ClipData> GetClipsForGame(int gameId, int count);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration, int count);
```

### ClipData contains the following values
```csharp
string Id;
string Url;
string EmbedUrl;
int BroadcasterId;
string BroadcasterName;
int CreatorId;
string CreatorName;
string VideoId;
string GameId;
string Language;
string Title;
int ViewCount;
DateTime CreatedAt;
string ThumbnailUrl;
float Duration;
```

## Markers
```csharp
StreamMarker CreateStreamMarker(string description);
```

### StreamMarker is the following class
```csharp
public class StreamMarker
{
	public int Id { get; set; }
    public DateTime CreatedAt { get; set; }
    public string Description { get; set; }
    public int Position { get; set; }
}
```

## Run Commercial
```csharp
void TwitchRunCommercial(int duration);
```

## Slow Mode
```csharp
void TwitchSlowMode(bool enabled = true, int duration = 0);
```

## Stream Update
```csharp
bool SetChannelTitle(string title);
GameInfo SetChannelGame(string game);
bool SetChannelGameById(string gameId);
```

## Announcement
> Supported color values are `blue`, `orange`, `green`, `purple`
{.is-success}

```csharp
void TwitchAnnounce(string message, bool bot = false, string color = null);
```

## OAuth & Client Id
```csharp
string TwitchOAuthToken;
```
```csharp
string TwitchClientId;
```

## User Variables
```csharp
T GetTwitchUserVar<T>(string userName, string varName, bool persisted = true);
void SetTwitchUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetTwitchUserVar(string userName, string varName, bool persisted = true);
void UnsetTwitchUser(string userName, bool persisted = true);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}