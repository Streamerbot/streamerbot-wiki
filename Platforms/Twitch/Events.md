---
title: Twitch Events
description: Reference of all available Twitch events
published: true
date: 2023-04-27T14:41:37.519Z
tags: twitch, events, reference
editor: markdown
dateCreated: 2022-07-13T18:55:36.587Z
---

Streamer.bot constantly listens for events from your configured Twitch account and can perform actions for each of them.

> Some Twitch events may require [Affiliate](https://help.twitch.tv/s/article/twitch-affiliate-program-faq) status and some may be unavailable if prohibited by local laws.
{.is-info}

## Standard Variables
### User
User variables are added when a specific person invokes it, this is with chat messages, cheers, whispers, etc. when something like a Ad Run, Present Viewers event triggers it won't generate variables because these aren't user specific.

Name | Description
----:|:------------
`user` | The user that followed the broadcaster
`userName` | The login name of the user that followed the broadcaster
`userId` | Unique user identifier
`userType` | Which streaming service the triggering user is coming from <br> `twitch` or `youtube`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
`userPreviousActive` | When the user was previously active
`eventSource` | specifies which streaming service the triggering event is coming from <br> `twitch` or `youtube`
{.vars-table}

### Broadcaster
This is always generated with Twitch events.

Name | Description
----:|:------------
`broadcastUser` | The Twitch display name of the broadcaster account
`broadcastUserName` | The Twitch user name of the broadcaster account
`broadcastUserId` | The Twitch user ID of the broadcaster account
`broadcastIsAffiliate` | Boolean value indicating if the broadcast account is a Twitch affiliate <br> `True` / `False`
`broadcastIsPartner` | Boolean value indicating if the broadcast account is a Twitch partner <br> `True` / `False`
{.vars-table}

## General
Configurable events in the *Platforms > Twitch > Events > General* tab{.subtitle}

- [<i class="mdi mdi-account text--twitch"></i> **Follows *When someone follows the broadcast user***](/Platforms/Twitch/Events/Follows)
- [<i class="mdi mdi-account-voice text--twitch"></i> **Whispers *When you receive a non-command whisper***](/Platforms/Twitch/Events/Whispers)
- [<i class="mdi mdi-comment-outline text--twitch"></i> **Chat Message *Receival of Chat Messages in the Broadcaster's chat***](/Platforms/Twitch/Events/Chat-Message)
- [<i class="mdi mdi-bullhorn text--twitch"></i> **Announcement *Twitch Chat announcements***](/Platforms/Twitch/Events/Announcement)
- [<i class="mdi mdi-account-star text--twitch"></i> **Shoutout Created *When a shoutout gets created on your channel***](/Platforms/Twitch/Events/Shoutout-Created)
- [<i class="mdi mdi-account-star text--twitch"></i> **Shoutout Received *When you receive a shoutout from an other streamer***](/Platforms/Twitch/Events/Shoutout-Received)
- [<i class="mdi mdi-numeric-1-box text--twitch"></i> **First Words *First words of the stream for individual users***](/Platforms/Twitch/Events/First-Words)
- [<i class="mdi mdi-account-multiple text--twitch"></i> **Present Viewers *This event occurs every 5 minutes***](/Platforms/Twitch/Events/Present-Viewers)
- [<i class="mdi mdi-television-classic text--twitch"></i> **Ad Run *When an ad runs on your channel***](/Platforms/Twitch/Events/Ad-Run)
- [<i class="mdi mdi-television-classic text--twitch"></i> **Ad Midroll *When an ad runs on your channel in the middle of streams*** *v0.1.15*{.version-badge}](/Platforms/Twitch/Events/Ad-Midroll)
{.btn-grid .my-5}

## Moderation
Configurable events in the *Platforms > Twitch > Moderation* tab{.subtitle}

- [<i class="mdi mdi-comment-remove-outline text--twitch"></i> **Message Deleted *When a message is deleted in your twitch chat***](/Platforms/Twitch/Events/Message-Deleted)
- [<i class="mdi mdi-account-minus text--twitch"></i> **User Banned *When a user is banned***](/Platforms/Twitch/Events/User-Banned)
- [<i class="mdi mdi-account-tie-voice-off text--twitch"></i> **User Timed Out *When a user is timed out***](/Platforms/Twitch/Events/User-Timed-Out)
- [<i class="mdi mdi-shield text--twitch"></i> **Shield Mode Begin *Shield Mode has begun*** *v0.1.15*{.version-badge}](/Platforms/Twitch/Events/Shield-Mode-Begin){.disabled}
- [<i class="mdi mdi-shield text--twitch"></i> **Shield Mode End *Shield Mode has ended*** *v0.1.15*{.version-badge}](/Platforms/Twitch/Events/Shield-Mode-End){.disabled}
{.btn-grid .my-5}

## Channel
Configurable events in the *Platforms > Twitch > Channel* tab{.subtitle}

* [<i class="mdi mdi-calendar-check-outline text--twitch"></i> **Stream Online *When you start streaming*** *v0.1.17*{.version-badge}](/Platforms/Twitch/Events/Stream-Online)
* [<i class="mdi mdi-calendar-remove-outline text--twitch"></i> **Stream Offline *When you stop streaming*** *v0.1.17*{.version-badge}](/Platforms/Twitch/Events/Stream-Offline)
{.btn-grid .my-5}

## Bot
Configurable events in the *Platforms > Twitch > Bot* tab{.subtitle}

- [<i class="mdi mdi-account-voice text--twitch"></i> **Whispers *When you receive a non-command whisper on your bot account***](/Platforms/Twitch/Events/Bot-Whispers){.disabled}
{.btn-grid .my-5}

## Standard Twitch Events
Configurable events in the *Platforms > Twitch > Events* tab{.subtitle}

- [<i class="mdi mdi-diamond-stone text--twitch"></i> **Cheers *Bit Cheer events***](/Platforms/Twitch/Events/Cheers)
- [<i class="mdi mdi-account-star-outline text--twitch"></i> **Sub *First time subscribers***](/Platforms/Twitch/Events/Sub)
- [<i class="mdi mdi-account-star text--twitch"></i> **Re-Sub *Users renewing their own subscription***](/Platforms/Twitch/Events/Sub)
- [<i class="mdi mdi-wallet-giftcard text--twitch"></i> **Gift Sub *Gifting a subscription to a named person***](/Platforms/Twitch/Events/Gift-Sub)
- [<i class="mdi mdi-gift text--twitch"></i> **Gift Bomb *Gifting 1 or more subscriptions to random users***](/Platforms/Twitch/Events/Gift-Bomb)
- [<i class="mdi mdi-target-account text--twitch"></i> **Raid *Incoming and Outgoing Raids***](/Platforms/Twitch/Events/Raid)
- [<i class="mdi mdi-train text--twitch"></i> **Hype Train *Start/end, progression, and level-up events***](/Platforms/Twitch/Events/Hype-Train)
- [<i class="mdi mdi-charity text--twitch"></i> **Charity *This has the Donation and Completed event*** *v0.1.15*{.version-badge}](/Platforms/Twitch/Events/Charity)
- [<i class="mdi mdi-progress-check text--twitch"></i> **Community Goal *When Community Goals are Started or Progressed***](/Platforms/Twitch/Events/Community-Goal)
- [<i class="mdi mdi-update text--twitch"></i> **Stream Update *When the Stream Category or Title changes***](/Platforms/Twitch/Events/Stream-Update)
{.btn-grid .my-5}

## Additional Event Types
*These event sources each have their own configuration tabs* {.subtitle}

- [<i class="mdi mdi-adjust text--twitch"></i>**Channel Point Rewards *Execute actions on point redemptions***](/Platforms/Twitch/Channel-Point-Rewards)
- [<i class="mdi mdi-poll text--twitch"></i>**Polls *Integration with Twitch Polls***](/Platforms/Twitch/Polls)
- [<i class="mdi mdi-poll mdi-flip-h text--twitch"></i>**Predictions *Integration with Twitch Predictions***](/Platforms/Twitch/Predictions)
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch *Go Back***](/Platforms/Twitch)
- [<i class="mdi mdi-twitch text--twitch"></i>**Twitch Sub-Actions *Up Next***](/Sub-Actions/Twitch)
{.btn-grid .my-5}