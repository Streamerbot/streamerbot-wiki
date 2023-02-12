---
title: WebSocket Server Events (PRIVATE)
description: Documentation of events that are emitted by the Streamer.bot WebSocket Server
published: false
date: 2023-02-12T22:58:03.809Z
tags: 
editor: markdown
dateCreated: 2023-02-07T23:13:42.483Z
---

## Event Output Format
### Tab {.tabset}
#### Schema
```json
{
    "timeStamp": ISO 8601 DateTime,
    "event": {
        "source": string
        "type": string
    },
    "data": {.object.} /* see information below for what this can contain */
}
```

#### Example

```json
{
    "timeStamp": "2022-01-30T21:32:04.4588947-05:00",
    "event": {
        "source": "Twitch",
        "type": "ChatMessage"
    },
    "data": {.object.}
}
```

## twitch
* [**AdMidRoll**](/Servers-Clients/WebSocket-Server/Events/twitch/AdMidRoll)
* [**AdRun**](/Servers-Clients/WebSocket-Server/Events/twitch/AdRun)
* [**Announcement**](/Servers-Clients/WebSocket-Server/Events/twitch/Announcement)
* [**BotWhisper**](/Servers-Clients/WebSocket-Server/Events/twitch/BotWhisper)
* [**BroadcastUpdate**](/Servers-Clients/WebSocket-Server/Events/twitch/BroadcastUpdate)
* [**CharityCompleted**](/Servers-Clients/WebSocket-Server/Events/twitch/CharityCompleted)
* [**CharityDonation**](/Servers-Clients/WebSocket-Server/Events/twitch/CharityDonation)
* [**CharityProgress**](/Servers-Clients/WebSocket-Server/Events/twitch/CharityProgress)
* [**CharityStarted**](/Servers-Clients/WebSocket-Server/Events/twitch/CharityStarted)
* [**ChatCleared**](/Servers-Clients/WebSocket-Server/Events/twitch/ChatCleared)
* [**ChatMessage**](/Servers-Clients/WebSocket-Server/Events/twitch/ChatMessage)
* [**ChatMessageDeleted**](/Servers-Clients/WebSocket-Server/Events/twitch/ChatMessageDeleted)
* [**Cheer**](/Servers-Clients/WebSocket-Server/Events/twitch/Cheer)
* [**CoinCheer**](/Servers-Clients/WebSocket-Server/Events/twitch/CoinCheer)
* [**CommunityGoalContribution**](/Servers-Clients/WebSocket-Server/Events/twitch/CommunityGoalContribution)
* [**CommunityGoalEnded**](/Servers-Clients/WebSocket-Server/Events/twitch/CommunityGoalEnded)
* [**FirstWord**](/Servers-Clients/WebSocket-Server/Events/twitch/FirstWord)
* [**Follow**](/Servers-Clients/WebSocket-Server/Events/twitch/Follow)
* [**GiftBomb**](/Servers-Clients/WebSocket-Server/Events/twitch/GiftBomb)
* [**GiftSub**](/Servers-Clients/WebSocket-Server/Events/twitch/GiftSub)
* [**GoalBegin**](/Servers-Clients/WebSocket-Server/Events/twitch/GoalBegin)
* [**GoalEnd**](/Servers-Clients/WebSocket-Server/Events/twitch/GoalEnd)
* [**GoalProgress**](/Servers-Clients/WebSocket-Server/Events/twitch/GoalProgress)
* [**HypeTrainEnd**](/Servers-Clients/WebSocket-Server/Events/twitch/HypeTrainEnd)
* [**HypeTrainLevelUp**](/Servers-Clients/WebSocket-Server/Events/twitch/HypeTrainLevelUp)
* [**HypeTrainStart**](/Servers-Clients/WebSocket-Server/Events/twitch/HypeTrainStart)
* [**HypeTrainUpdate**](/Servers-Clients/WebSocket-Server/Events/twitch/HypeTrainUpdate)
* [**PollCompleted**](/Servers-Clients/WebSocket-Server/Events/twitch/PollCompleted)
* [**PollCreated**](/Servers-Clients/WebSocket-Server/Events/twitch/PollCreated)
* [**PollUpdated**](/Servers-Clients/WebSocket-Server/Events/twitch/PollUpdated)
* [**PredictionCanceled**](/Servers-Clients/WebSocket-Server/Events/twitch/PredictionCanceled)
* [**PredictionCompleted**](/Servers-Clients/WebSocket-Server/Events/twitch/PredictionCompleted)
* [**PredictionCreated**](/Servers-Clients/WebSocket-Server/Events/twitch/PredictionCreated)
* [**PredictionLocked**](/Servers-Clients/WebSocket-Server/Events/twitch/PredictionLocked)
* [**PredictionUpdated**](/Servers-Clients/WebSocket-Server/Events/twitch/PredictionUpdated)
* [**PresentViewers** *BROKEN*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/twitch/PresentViewers)
* [**Raid**](/Servers-Clients/WebSocket-Server/Events/twitch/Raid)
* [**ReSub**](/Servers-Clients/WebSocket-Server/Events/twitch/ReSub)
* [**RewardCreated**](/Servers-Clients/WebSocket-Server/Events/twitch/RewardCreated)
* [**RewardDeleted**](/Servers-Clients/WebSocket-Server/Events/twitch/RewardDeleted)
* [**RewardRedemption**](/Servers-Clients/WebSocket-Server/Events/twitch/RewardRedemption)
* [**RewardUpdated**](/Servers-Clients/WebSocket-Server/Events/twitch/RewardUpdated)
* [**ShieldModeBegin**](/Servers-Clients/WebSocket-Server/Events/twitch/ShieldModeBegin)
* [**ShieldModeEnd**](/Servers-Clients/WebSocket-Server/Events/twitch/ShieldModeEnd)
* [**ShoutoutCreated**](/Servers-Clients/WebSocket-Server/Events/twitch/ShoutoutCreated)
* [**ShoutoutReceived**](/Servers-Clients/WebSocket-Server/Events/twitch/ShoutoutReceived)
* [**StreamOffline**](/Servers-Clients/WebSocket-Server/Events/twitch/StreamOffline)
* [**StreamOnline** *BROKEN*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/twitch/StreamOnline)
* [**StreamUpdate**](/Servers-Clients/WebSocket-Server/Events/twitch/StreamUpdate)
* [**StreamUpdateGameOnConnect**](/Servers-Clients/WebSocket-Server/Events/twitch/StreamUpdateGameOnConnect)
* [**Sub**](/Servers-Clients/WebSocket-Server/Events/twitch/Sub)
* [**SubCounterRollover**](/Servers-Clients/WebSocket-Server/Events/twitch/SubCounterRollover)
* [**UserBanned**](/Servers-Clients/WebSocket-Server/Events/twitch/UserBanned)
* [**UserTimedOut**](/Servers-Clients/WebSocket-Server/Events/twitch/UserTimedOut)
* [**UserUntimedOut**](/Servers-Clients/WebSocket-Server/Events/twitch/UserUntimedOut)
* [**Whisper**](/Servers-Clients/WebSocket-Server/Events/twitch/Whisper)
{.btn-grid .my-5}

## youTube
* [**BroadcastEnded**](/Servers-Clients/WebSocket-Server/Events/youTube/BroadcastEnded)
* [**BroadcastStarted**](/Servers-Clients/WebSocket-Server/Events/youTube/BroadcastStarted)
* [**BroadcastUpdated**](/Servers-Clients/WebSocket-Server/Events/youTube/BroadcastUpdated)
* [**FirstWords**](/Servers-Clients/WebSocket-Server/Events/youTube/FirstWords)
* [**GiftMembershipReceived**](/Servers-Clients/WebSocket-Server/Events/youTube/GiftMembershipReceived)
* [**MemberMileStone**](/Servers-Clients/WebSocket-Server/Events/youTube/MemberMileStone)
* [**MembershipGift**](/Servers-Clients/WebSocket-Server/Events/youTube/MembershipGift)
* [**Message**](/Servers-Clients/WebSocket-Server/Events/youTube/Message)
* [**MessageDeleted**](/Servers-Clients/WebSocket-Server/Events/youTube/MessageDeleted)
* [**NewSponsor**](/Servers-Clients/WebSocket-Server/Events/youTube/NewSponsor)
* [**NewSponsorOnlyEnded**](/Servers-Clients/WebSocket-Server/Events/youTube/NewSponsorOnlyEnded)
* [**NewSponsorOnlyStarted**](/Servers-Clients/WebSocket-Server/Events/youTube/NewSponsorOnlyStarted)
* [**PresentViewers**](/Servers-Clients/WebSocket-Server/Events/youTube/PresentViewers)
* [**StatisticsUpdated**](/Servers-Clients/WebSocket-Server/Events/youTube/StatisticsUpdated)
* [**SuperChat**](/Servers-Clients/WebSocket-Server/Events/youTube/SuperChat)
* [**SuperSticker**](/Servers-Clients/WebSocket-Server/Events/youTube/SuperSticker)
* [**UserBanned**](/Servers-Clients/WebSocket-Server/Events/youTube/UserBanned)
{.btn-grid .my-5}

{.btn-grid .my-5}

## application
* [**ActionAdded**](/Servers-Clients/WebSocket-Server/Events/application/ActionAdded)
* [**ActionDeleted**](/Servers-Clients/WebSocket-Server/Events/application/ActionDeleted)
* [**ActionUpdated**](/Servers-Clients/WebSocket-Server/Events/application/ActionUpdated)
{.btn-grid .my-5}

## raw
* [**Action**](/Servers-Clients/WebSocket-Server/Events/raw/Action)
* [**ActionCompleted**](/Servers-Clients/WebSocket-Server/Events/raw/ActionCompleted)
* [**SubAction**](/Servers-Clients/WebSocket-Server/Events/raw/SubAction)
{.btn-grid .my-5}

## command
* [**BotWhisper**](/Servers-Clients/WebSocket-Server/Events/command/BotWhisper)
* [**Message**](/Servers-Clients/WebSocket-Server/Events/command/Message)
* [**MessageCooldown**](/Servers-Clients/WebSocket-Server/Events/command/MessageCooldown)
* [**Whisper**](/Servers-Clients/WebSocket-Server/Events/command/Whisper)
{.btn-grid .my-5}

## donorDrive
* [**Donation**](/Servers-Clients/WebSocket-Server/Events/donorDrive/Donation)
* [**Incentive**](/Servers-Clients/WebSocket-Server/Events/donorDrive/Incentive)
* [**ProfileUpdated**](/Servers-Clients/WebSocket-Server/Events/donorDrive/ProfileUpdated)
{.btn-grid .my-5}

## fileWatcher
* [**Changed**](/Servers-Clients/WebSocket-Server/Events/fileWatcher/Changed)
* [**Created**](/Servers-Clients/WebSocket-Server/Events/fileWatcher/Created)
* [**Deleted**](/Servers-Clients/WebSocket-Server/Events/fileWatcher/Deleted)
* [**Renamed**](/Servers-Clients/WebSocket-Server/Events/fileWatcher/Renamed)
{.btn-grid .my-5}

## general
* [**Custom**](/Servers-Clients/WebSocket-Server/Events/general/Custom)
{.btn-grid .my-5}

## hypeRate
* [**HeartRatePulse**](/Servers-Clients/WebSocket-Server/Events/hypeRate/HeartRatePulse)
{.btn-grid .my-5}

## kofi
* [**Commission**](/Servers-Clients/WebSocket-Server/Events/kofi/Commission)
* [**Donation**](/Servers-Clients/WebSocket-Server/Events/kofi/Donation)
* [**Resubscription**](/Servers-Clients/WebSocket-Server/Events/kofi/Resubscription)
* [**ShopOrder**](/Servers-Clients/WebSocket-Server/Events/kofi/ShopOrder)
* [**Subscription**](/Servers-Clients/WebSocket-Server/Events/kofi/Subscription)
{.btn-grid .my-5}

## midi
* [**Message**](/Servers-Clients/WebSocket-Server/Events/midi/Message)
{.btn-grid .my-5}

## misc
* [**PyramidBroken**](/Servers-Clients/WebSocket-Server/Events/misc/PyramidBroken)
* [**PyramidSuccess**](/Servers-Clients/WebSocket-Server/Events/misc/PyramidSuccess)
* [**TimedAction**](/Servers-Clients/WebSocket-Server/Events/misc/TimedAction)
{.btn-grid .my-5}

## obs
* [**Connected**](/Servers-Clients/WebSocket-Server/Events/obs/Connected)
* [**Disconnected**](/Servers-Clients/WebSocket-Server/Events/obs/Disconnected)
{.btn-grid .my-5}

## patreon
* [**FollowCreated**](/Servers-Clients/WebSocket-Server/Events/patreon/FollowCreated)
* [**FollowDeleted**](/Servers-Clients/WebSocket-Server/Events/patreon/FollowDeleted)
* [**PledgeCreated**](/Servers-Clients/WebSocket-Server/Events/patreon/PledgeCreated)
* [**PledgeDeleted**](/Servers-Clients/WebSocket-Server/Events/patreon/PledgeDeleted)
* [**PledgeUpdated**](/Servers-Clients/WebSocket-Server/Events/patreon/PledgeUpdated)
{.btn-grid .my-5}

## pulsoid
* [**HeartRatePulse**](/Servers-Clients/WebSocket-Server/Events/pulsoid/HeartRatePulse)
{.btn-grid .my-5}

## quote
* [**Added** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/quote/Added){.disabled}
* [**Show** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/quote/Show){.disabled}
{.btn-grid .my-5}

## shopify
* [**OrderCreated**](/Servers-Clients/WebSocket-Server/Events/shopify/OrderCreated)
* [**OrderPaid**](/Servers-Clients/WebSocket-Server/Events/shopify/OrderPaid)
{.btn-grid .my-5}

## speechToText
* [**Command**](/Servers-Clients/WebSocket-Server/Events/speechToText/Command)
* [**Dictation**](/Servers-Clients/WebSocket-Server/Events/speechToText/Dictation)
{.btn-grid .my-5}

## streamElements
* [**Merch**](/Servers-Clients/WebSocket-Server/Events/streamElements/Merch)
* [**Tip**](/Servers-Clients/WebSocket-Server/Events/streamElements/Tip)
{.btn-grid .my-5}

## streamlabs
* [**Donation**](/Servers-Clients/WebSocket-Server/Events/streamlabs/Donation)
* [**Merchandise**](/Servers-Clients/WebSocket-Server/Events/streamlabs/Merchandise)
{.btn-grid .my-5}

## tipeeeStream
* [**Donation**](/Servers-Clients/WebSocket-Server/Events/tipeeeStream/Donation)
{.btn-grid .my-5}

## treatStream
* [**Treat**](/Servers-Clients/WebSocket-Server/Events/treatStream/Treat)
{.btn-grid .my-5}

## websocketClient
* [**Close** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/websocketClient/Close){.disabled}
* [**Message** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/websocketClient/Message){.disabled}
* [**Open** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/websocketClient/Open){.disabled}
{.btn-grid .my-5}

## websocketCustomServer
* [**Close** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/websocketCustomServer/Close){.disabled}
* [**Message** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/websocketCustomServer/Message){.disabled}
* [**Open** *NOT BROADCAST*{.version-badge}](/Servers-Clients/WebSocket-Server/Events/websocketCustomServer/Open){.disabled}
{.btn-grid .my-5}