---
title: YouTube Event Reference
description: Reference of all variables available for the YouTube platform
published: true
date: 2023-02-05T01:22:59.078Z
tags: youtube, variables, arguments
editor: markdown
dateCreated: 2022-06-23T02:31:00.996Z
---

> All events will also include the user variables outlined below
{.is-success}

Name | Description
----:|:------------
`user` | The user that activated this event
`userName` | User login name <br> `lowercase`
`userId` | Unique user identifier
`userType` | Specifies which streaming service the triggering user is coming from <br> `twitch` or `youtube`
`userProfileUrl` | The user's profile picture URL<br>
`isSubscribed` | Boolean value indicating if the user is a member on your channel <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
`broadcastUserName` | The username of the broadcaster<br>
`broadcastUserId` | The id of the broadcaster<br>
`broadcastUserProfileImage` | The profile picture of the broadcaster<br>
{.vars-table}

## Generic Events
* [<i class="mdi mdi-comment-outline text--youtube"></i> **Chat Message *Receival of Chat Messages in the Broadcaster's chat***](/Platforms/YouTube/Events/Chat-Message)
* [<i class="mdi mdi-numeric-1-box text--youtube"></i> **First Words *First words of the stream for individual users***](/Platforms/YouTube/Events/First-Words)
* [<i class="mdi mdi-account-plus text--youtube"></i> **Member Milestone Event**](/Platforms/YouTube/Events/Member-Milestone-Event)
* [<i class="mdi mdi-account-remove text--youtube"></i> **User Banned Event *When a user gets banned***](/Platforms/YouTube/Events/User-Banned-Event)
* [<i class="mdi mdi-account-plus text--youtube"></i> **Membership Gift Event *When someone gifts a membership to someone***](/Platforms/YouTube/Events/Membership-Gift-Event)
* [<i class="mdi mdi-account-plus text--youtube"></i> **Gift Membership Received Event *When someone receives a membership from someone***](/Platforms/YouTube/Events/Gift-Membership-Received-Event)
* [<i class="mdi mdi-account-multiple text--youtube"></i> **Present Viewers *An event every 1-10 minutes indicating your present viewers***](/Platforms/YouTube/Events/Present-Viewers)
{.btn-grid .my-5}

## Sponsor Events
* [<i class="mdi mdi-cash text--youtube"></i> **Sponsor Event**](/Platforms/YouTube/Events/Sponsor-Event)
* [<i class="mdi mdi-cash text--youtube"></i> **Sponsor Mode Only Started**](/Platforms/YouTube/Events/Sponsor-Mode-Only-Started)
* [<i class="mdi mdi-cash text--youtube"></i> **Sponsor Mode Only Ended**](/Platforms/YouTube/Events/Sponsor-Mode-Only-Ended)
{.btn-grid .my-5}

## Super Events
* [<i class="mdi mdi-comment-outline text--youtube"></i> **Super Chat**](/Platforms/YouTube/Events/Super-Chat)
* [<i class="mdi mdi-sticker text--youtube"></i> **Super Sticker**](/Platforms/YouTube/Events/Super-Sticker)
{.btn-grid .my-5}

## Broadcast Events
* [<i class="mdi mdi-calendar-check-outline text--youtube"></i> **Broadcast Started *When the broadcast starts***](/Platforms/YouTube/Events/Broadcast-Started)
* [<i class="mdi mdi-calendar-remove-outline text--youtube"></i> **Broadcast Ended *When the broadcast end***](/Platforms/YouTube/Events/Broadcast-Ended)
* [<i class="mdi mdi-calendar text--youtube"></i> **Broadcast Update *When the broadcast configuration updates***](/Platforms/YouTube/Events/Broadcast-Update)
* [<i class="mdi mdi-microsoft-excel text--youtube"></i> **Statistics Update *When the statistics of your stream updates***](/Platforms/YouTube/Events/Statistics-Update)
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/Events)
{.btn-grid .my-5}