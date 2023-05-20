---
title: Twitch
description: C# Available Methods Reference
published: true
date: 2023-05-13T03:43:29.661Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:51:36.923Z
---

## General
```csharp
void TwitchSubscriberOnly(bool enabled = true);
void TwitchEmoteOnly(bool enabled = true);
void TwitchSlowMode(bool enabled = true, int duration = 0);
void TwitchFollowMode(bool enabled = true, int duration = 0);
```

## User Information
```csharp
// Added in v0.1.18
bool TwitchIsUserSubscribed(string userId, out string tier);
```

## Cheermotes
```csharp
List<Cheermote> GetCheermotes();
```

## Whisper
```csharp
bool SendWhisper(string userName, string message, bool bot = true);
```

## Moderator
```csharp
bool TwitchAddModerator(string userName);
bool TwitchRemoveModerator(string userName);
```

## Vip
```csharp
bool TwitchAddVip(string userName);
bool TwitchRemoveVip(string userName);
```

## Messages
```csharp
void SendMessage(string message, bool bot = true);
void SendAction(string action, bool bot = true);
```

```csharp
bool TwitchClearChatMessages(bool bot = true);
bool TwitchDeleteChatMessage(string messageId, bool bot = true);
```

## Channel Tags
```csharp
bool TwitchClearChannelTags();
bool TwitchSetChannelTags(List<string> tags);
bool TwitchAddChannelTag(string tag);
bool TwitchRemoveChannelTag(string tag);
```
> Clearing tags is currently broken on Twitch's side, as long as you keep at least 1 tag, everything will work.  Unknown when Twitch will fix this
{.is-warning}

## Shoutout
```csharp
bool TwitchSendShoutoutById(string userId);
bool TwitchSendShoutoutByLogin(string userLogin);
```

## Timeouts / Bans
```csharp
bool TwitchBanUser(string userName, string reason = null, bool bot = false);
```

```csharp
// This will unban and untimeout users
bool TwitchUnbanUser(string userName, bool bot = false);
```

```csharp
// A duration of 0 will result in a ban
bool TwitchTimeoutUser(string username, int duration, string reason = null, bool bot = false);
```

## Channel Rewards
### Get Rewards
```csharp
// Added in v0.1.18
List<TwitchReward> TwitchGetRewards();
```

Structure of TwitchReward:
```csharp
public class TwitchReward
{
    public string Id { get; set; }
    public string Title { get; set; }
    public string Prompt { get; set; }
    public int Cost { get; set; }
    public bool InputRequired { get; set; }
    public string BackgroundColor { get; set; }
    public bool Paused { get; set; }
    public bool Enabled { get; set; }
    public bool IsOurs { get; set; }
}
```

### Get Reward Usage
```csharp
long TwitchGetChannelPointsUsedByUserId(string userId);
```

### Reward States
```csharp
void DisableReward(string rewardId);
void EnableReward(string rewardId);
void PauseReward(string rewardId);
void UnPauseReward(string rewardId);
```

### Reward Group States
```csharp
void TwitchRewardGroupEnable(string groupName);
void TwitchRewardGroupDisable(string groupName);
void TwitchRewardGroupToggleEnable(string groupName);
void TwitchRewardGroupPause(string groupName);
void TwitchRewardGroupUnPause(string groupName);
void TwitchRewardGroupTogglePause(string groupName);
```

### Update Rewards
```csharp
bool UpdateRewardTitle(string rewardId, string title);
bool UpdateRewardPrompt(string rewardId, string prompt);
void UpdateRewardCost(string rewardId, int cost, bool additive = false);
void UpdateRewardCooldown(string rewardId, int cooldown, bool additive = false);
bool UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null);
```

### Fulfill/Cancel
```csharp
bool TwitchRedemptionFulfill(string rewardId, string redemptionId);
bool TwitchRedemptionCancel(string rewardId, string redemptionId);
```

### Reset Reward Counters
```csharp
void TwitchResetRewardCounter(string rewardId);
void TwitchResetRewardUserCounters(string rewardId);
void TwitchResetUserRewardCounters(string userId, bool persisted);
void TwitchResetUserRewardCounter(string rewardId, string userId);
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

## Bits
```csharp
// Added in v0.1.18
long TwitchGetBitsDonatedByUserId(string userId);
```

## Get Clips
> All clip data is sorted by view count, this is a limitation of the Twitch API. To get most recent clips, one would have to get all the clips for the user, one got-ya for this, there is a hard limit of 1000 clips that can be returned
{.is-info}

### Get all clips
```csharp
List<ClipData> GetAllClips();
```

### Get clips for username
```csharp
List<ClipData> GetClipsForUser(string username);
List<ClipData> GetClipsForUser(string userName, int count);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(string username, TimeSpan duration);
List<ClipData> GetClipsForUser(string username, TimeSpan duration, int count);
```

### Get clips for user id
```csharp
List<ClipData> GetClipsForUser(int userId);
List<ClipData> GetClipsForUser(int userId, int count);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration, int count);
```

### Get clips for game
```csharp
List<ClipData> GetClipsForGame(int gameId);
List<ClipData> GetClipsForGame(int gameId, int count);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration, int count);
```

## Create Clip
```csharp
ClipData CreateClip();
```

ClipData contains the following values:
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

## Stream Information
```csharp
bool SetChannelTitle(string title);
GameInfo SetChannelGame(string game);
bool SetChannelGameById(string gameId);
```

## Raids
```csharp
bool TwitchStartRaidById(string userId);
bool TwitchStartRaidByName(string userName);
bool TwitchCancelRaid();
```

## Announcement
> Supported color values are `blue`, `orange`, `green`, `purple`
{.is-success}

```csharp
void TwitchAnnounce(string message, bool bot = false, string color = null);
```

## Team Information
```csharp
List<TeamInfo> GetTeamInfoById(string userId);
List<TeamInfo> GetTeamInfoByLogin(string userLogin);
```

```csharp
public class TeamInfo
{
    public string Id { get; set; }
    public string Login { get; set; }
    public string Name { get; set; }

    public string BackgroundImageUrl { get; set; }
    public string Banner { get; set; }

    public string CreatedAt { get; set; }
    public string UpdatedAt { get; set; }

    public string Info { get; set; }
    public string ThumbnailUrl { get; set; }
    public string TeamName { get; set; }
    public string TeamDisplayName { get; set; }
    public string TeamId { get; set; }
}
```


## OAuth & Client Id
```csharp
string TwitchOAuthToken;
```
```csharp
string TwitchClientId;
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}