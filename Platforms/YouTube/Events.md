---
title: YouTube Event Variables
description: Reference of all variables available for the YouTube platform
published: true
date: 2022-09-28T08:31:13.005Z
tags: youtube, variables, arguments
editor: markdown
dateCreated: 2022-06-23T02:31:00.996Z
---

All events will also have the typical user information

> **Note:**
> `isSubscribed` won't work but you will get the variable anyways, so that's why it's in this list below.
{.is-info}

Name | Description
----:|:------------
`user` | The user that activated this event
`userName` | User login name <br> `lowercase`
`userId` | Unique user identifier
`userType` | Specifies which streaming service the triggering user is coming from <br> `twitch` or `youtube`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
{.vars-table}

## Broadcast Started
Name | Description
----:|:------------
`title` | The title of the broadcast
`description` | The description of the broadcast
`publishedAt` | The time the broadcast was published at
`broadcastId` | The id of the broadcast

## Broadcast Ended
No variables

## Message
Name | Description
----:|:------------
`messageId` | The id of the message
`message` | The message sent to the chat
`publishedAt` | The time the message was published at

## User Banned
Name | Description
----:|:------------
`banType` | The type of ban
`banDuration` | The duration of the ban

## Super Chat
Name | Description
----:|:------------
`messageId` | The id of the super chat event
`message` | The message of the super chat event
`publishedAt` | The time the super chat event was published at
`tier` | The tier for the paid message
`amount` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user.
`microAmount` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000.
`currencyCode` | The currency in which the purchase was made. The value is an ISO 4217 currency code.

## Super Sticker
Name | Description
----:|:------------
`messageId` | The id of the super sticker event
`publishedAt` | The time the super sticker event was published at
`tier` | The tier for the paid message
`amount` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user.
`microAmount` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000.
`currencyCode` | The currency in which the purchase was made. The value is an ISO 4217 currency code.
`stickerId` | A unique ID that identifies the sticker image.
`stickerAltText` | A text string that describes the sticker.
`stickerLanguage` | The language of the `stickerAltText`

## Sponsor
Name | Description
----:|:------------
`messageId` | The id of the sponsor event
`publishedAt` | The time the sponsor event was published at
`isUpgrade` | Indicates whether the viewer just upgraded from a lower level
`levelName` | The name of the Level at which the viewer is a member

## Member Milestone
Name | Description
----:|:------------
`messageId` | The id of the member milestone event
`publishedAt` | The time the member milestone event was published at
`months` | The total amount of months (rounded up) the viewer has been a member
`levelName` | The name of the Level at which the viewer is a member.
`message` | The message associated with the member milestone event

## Sponsor Only Mode Started
Name | Description
----:|:------------
`messageId` | The id of the sponsor only mode started event
`publishedAt` | The time the sponsor only mode event was published at


## Sponsor Only Mode Ended
Name | Description
----:|:------------
`messageId` | The id of the sponsor only mode ended sticker event
`publishedAt` | The time the sponsor only mode ended event was published at

## Membership Gifting
Name | Description
----:|:------------
`id` | The title of the broadcast
`count` | The description of the broadcast
`tier` | The time the broadcast was published at

## Gift Membership Received
Name | Description
----:|:------------
`id` | The id of the membership gifting event
`tier` | The tier the gifted user received
`gifterUser` | The display name of the user who received the gifted membership
`gifterUserName` | The user name of the user who received the gifted membership
`gifterUserId` | The id of the user who received the gifted membership
`gifterUserType` | The type of user who received the gifted membership

## Statistics Updated
This event is fired whenever any of the values below change.

Name | Description
----:|:------------
`likeCount` | The number of likes the broadcast has
`dislikeCount` | The number of dislikes the broadcast has
`viewCount` | The number of viewers the broadcast has had
`commentCount` | The number of comments added to the broadcast
`favoriteCount` | How many times the broadcast has been favorited

## Broadcast Update
This event is fired whenever any of the values below change.

Name | Description
----:|:------------
`id` | The id of the broadcast
`title` | The title of the broadcast
`description` |The description of the broadcast
`privacy` | The privacy setting of the broadcast

> **Note**
> Coming soon
{.is-info}

## Generic Events
* [**Chat Message**](){.disabled}
* [**First Words**](){.disabled}
* [**Sponser Event**](){.disabled}
* [**Sponser Mode Only Started**](){.disabled}
* [**Sponser Mode Only Ended**](){.disabled}
* [**Member Milestone Event**](){.disabled}
* [**User Banned Event**](){.disabled}
* [**Membership Gift Event**](){.disabled}
* [**Gift Membership Event**](){.disabled}
{.btn-grid .my-5}

## Super Events
* [**Super Chat**](){.disabled}
* [**Super Sticker**](){.disabled}
{.btn-grid .my-5}

## Broadcast Events
* [**Broadcast Started**](){.disabled}
* [**Broadcast Ended**](){.disabled}
* [**Broadcast Update**](){.disabled}
* [**Statistics Update**](){.disabled}
{.btn-grid .my-5}