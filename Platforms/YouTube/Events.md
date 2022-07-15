---
title: YouTube Event Variables
description: Reference of all variables available for the YouTube platform
published: true
date: 2022-07-13T19:57:58.698Z
tags: youtube, variables, arguments
editor: markdown
dateCreated: 2022-06-23T02:31:00.996Z
---

All events will also have the typical user information
<br>

# Broadcast Started

| Variable | Description |
|  ---:|:--- |
| `%title%` | The title of the broadcast |
| `%description%` | The description of the broadcast |
| `%publishedAt%` | The time the broadcast was published at |
| `%broadcastId%` | The id of the broadcast |

# Broadcast Ended

No variables

# Message

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the message |
| `%message%` | The message sent to the chat |
| `%publishedAt%` | The time the message was published at |

# User Banned

| Variable | Description |
|  ---:|:--- |
| `%banType%` | The type of ban |
| `%banDuration%` | The duration of the ban |

# Super Chat

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the super chat event |
| `%message%` | The message of the super chat event |
| `%publishedAt%` | The time the super chat event was published at |
| `%tier%` | The tier for the paid message |
| `%amount%` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user. |
| `%microAmount%` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000. |
| `%currencyCode%` | The currency in which the purchase was made. The value is an ISO 4217 currency code. |

# Super Sticker

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the super sticker event |
| `%publishedAt%` | The time the super sticker event was published at |
| `%tier%` | The tier for the paid message |
| `%amount%` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user. |
| `%microAmount%` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000. |
| `%currencyCode%` | The currency in which the purchase was made. The value is an ISO 4217 currency code. |
| `%stickerId%` | A unique ID that identifies the sticker image. |
| `%stickerAltText%` | A text string that describes the sticker. |
| `%stickerLanguage%` | The language of the `%stickerAltText%` |

# Sponsor

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the sponsor event |
| `%publishedAt%` | The time the sponsor event was published at |
| `%isUpgrade%` | Indicates whether the viewer just upgraded from a lower level |
| `%levelName%` | The name of the Level at which the viewer is a member |

# Member Milestone

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the member milestone event |
| `%publishedAt%` | The time the member milestone event was published at |
| `%months%` | The total amount of months (rounded up) the viewer has been a member |
| `%levelName%` | The name of the Level at which the viewer is a member. |
| `%message%` | The message associated with the member milestone event |

# Sponsor Only Mode Started

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the sponsor only mode started event |
| `%publishedAt%` | The time the sponsor only mode event was published at |


# Sponsor Only Mode Ended

| Variable | Description |
|  ---:|:--- |
| `%messageId%` | The id of the sponsor only mode ended sticker event |
| `%publishedAt%` | The time the sponsor only mode ended event was published at |

# Membership Gifting

| Variable | Description |
|  ---:|:--- |
| `%id%` | The title of the broadcast |
| `%count%` | The description of the broadcast |
| `%tier%` | The time the broadcast was published at |

# Gift Membership Received

| Variable | Description |
|  ---:|:--- |
| `%id%` | The id of the membership gifting event |
| `%tier%` | The tier the gifted user received |
| `%gifterUser%` | The display name of the user who received the gifted membership |
| `%gifterUserName%` | The user name of the user who received the gifted membership |
| `%gifterUserId%` | The id of the user who received the gifted membership |
| `%gifterUserType%` | The type of user who received the gifted membership |

# Statistics Updated

This event is fired whenever any of the values below change.

| Variable | Description |
|  ---:|:--- |
| `%likeCount%` | The number of likes the broadcast has |
| `%dislikeCount%` | The number of dislikes the broadcast has |
| `%viewCount%` | The number of viewers the broadcast has had |
| `%commentCount%` | The number of comments added to the broadcast |
| `%favoriteCount%` | How many times the broadcast has been favorited |

# Broadcast Update

This event is fired whenever any of the values below change.

| Variable | Description |
|  ---:|:--- |
| `%id%` | The id of the broadcast |
| `%title%` | The title of the broadcast |
| `%description%` |The description of the broadcast |
| `%privacy%` | The privacy setting of the broadcast |