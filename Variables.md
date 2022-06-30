---
title: Variables
description: 
published: true
date: 2022-06-30T20:50:57.494Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:50.460Z
---

> This page will be revamped everything below is going to be changed
{.is-warning}

# Variables (Arguments)

Every event that `streamer.bot` can monitor generates an argument stack specific to that event that presents variable data to the action it calls. 

Below is a cheatsheat of the Generic arguments available to use in your [Sub-Actions](/Sub-Actions) and a description of their function. 
Most general use triggers will have all generic arguemnts listed, any exceptions will be listed on the page detailing that function
Events and sub-actions will add additional arguments to the stack but these are too numerous to list in one place so they will be detailed on the pages that cover those functions and will be hyperlinked.


This list is not exhaustive and some variables may work with sub-actions / events even though they do not specifically state compatibility

> If an action is not covered here yet, you can always use [Log All Arguments](/Sub-Actions/Code/Execute-CSharp-Code/Examples/Log-All-Arguments) in a sub-action to see what is available for use.
{.is-success}


***

## Tips

To use a variable / argument in most external contexts like OBS sources, bookend the variable name with a % symbol on either end - e.g. `%userName%`

> You do not need the % symbols for logic statements like `If` and `Global`
> This was required in older versions of `streamer.bot` and it will still work with them in but current version ignores these by default.
{.is-success}

***


> Arguments only persist until the called action finishes execution and can not be referenced by any other simultaneous action unless writen out to a `Global` variable
{.is-info}



> Variables are only populated into the active Arguments when the event or sub-action they are tied to executes. If you are testing and it is only returning the name of the variable you are probably not testing the complete Action / Event
{.is-success}


## Formatting Variables

> Variables can be formatted inline using standard C# notation
e.g. `%tipAmount%` will give a number but you could also use `%tipAmount:c2%` to have it formatted as a currency with 2 decimal places
Similarly `%time%` can be written `%time:t%` to have it formatted in short notation with AM/PM suffix
Further information on valid modifiers can be found [here](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings)
{.is-info}


***

# Generic


- [Generic](/en/Variables/Generic)
{.links-list}

Generic variables are available to most event sources, so consider these the minimum you can use. Other sources will expand on these with variables specific to that event or sub-action

Variable | Description | Notes
---------:|------------
`user` | User's Display Name | (**Note** this is case sensitive when using in a comparison)
`userType` | Specifies which streaming service the triggering user is coming from| <span style="color:blue">*(0.1.8+)*</span>  `twitch`,`youtube`
`userName` | User's Login Name |(**Note** this is all lowercase when using in a comparison for Twitch)
`userId` | Triggering user's unique ID
`isSubscribed` | Boolean for Twitch subscription status of triggering user | `True` / `False`
`isVip` | Boolean for Twitch VIP status of triggering user | `True` / `False`
`isModerator` | Boolean for Twitch moderator status of triggering user | `True` / `False`
`randomUser0` | The `username` of a random user present in chat |  <span style="color:blue">*(0.1.8+ does not include random users by default)*</span>
`randomUserName0` | The Display name of a random user present in chat |  <span style="color:blue">*(0.1.8+ does not include random users by default)*</span>
`__source` | The name of the event triggering the action
`date` | current system date | Accepts any standard formatting notation eg. `%date:yyyy/MM/dd%` or `%date:dddd, dd MMMM yyyy%`
`time` | current system time | Accepts any standard formtting notation eg. `HH-mm`
`actionId` | The unique ID number of the first action called |  <span style="color:blue">*(0.1.8+)*</span>
`runningActionId` | The instance ID number of the action in the queue | <span style="color:blue">*(0.1.8+)*</span>
`eventSource` | a string value to specify which platform generated the event| <span style="color:blue">*(0.1.8+)*</span> `twitch`, `youtube`

***

### Broadcaster Variables <span style="color:blue">*(0.1.5+)*</span>
If Twitch is connected, actions will have the following five variables available to them

From version <span style="color:blue">*(0.1.8+)*</span> you need to do a sub-action for this

| Variable | Description | Notes
|   ---:|-------------|
| `broadcastUser` | The Twitch display name of the broadcaster account |
| `broadcastUserName` | The Twitch user name of the broadcaster account |
| `broadcastUserId` | The Twitch user ID of the broadcaster account |
| `broadcastIsAffiliate` | Boolean value indicating if the broadcast account is a Twitch affiliate | `True` / `False`
| `broadcastIsPartner` | Boolean value indicating if the broadcast account is a Twitch partner | `True` / `False`

***


# Platform Events

## Twitch 


The arguments that each event adds to the stack will be detailed on the page that explains that function 

- [Follow *When someone follows your channel*](/en/Events/General)
- [Chat Message *When any chat message is recieved that does not contain a command*](/en/Events/General)
- [Whispers *When someone whispers your broadcaster account directly and does not contain a command*](/en/Events/General)
- [First Words *The first message a particular user sends to chat within the `Auto Reset` window*](/en/Events/General)
- [Cheers *When any chat message is recieved that contains bit cheermotes*](/en/Events/Cheers)
- [Subscriptions & Re-Subs *When someone subscribes or resubscribes to your channel themselves*](/en/Events/Sub)
- [Gift Subscriptions *When a user purchases a subscription for a specific **named** recipient*](/Events/Gift-Sub)
- [Gift Bombs *When a user purchases one or more subscriptions for **random** recipients*](/en/Events/Gift-Bomb)
- [Raids *When a user brings a raid into your channel or when you raid another user*](/en/Events/Raid)
- [Hosts *When a user begins hosting your channel*](/en/Events/hosts)
- [Hype Trains *Whenever a Hype Train is `Started`, `Ends` or is `Progressed`*](/en/Events/Hype-Train)
- [Community Goal *Whenever a user contributes to an active goal or one is ended*](/en/Events/Community-Goal)

{.links-list}






***

### [Channel Reward Redemption](/en/Twitch/Channel-Point-Rewards)

Variable | Description
---------:|------------
`redemptionId` | Twitch's internal ID for the redemption (used to refund reward)
`rewardId` | Twitch's internal ID of the reward
`rewardName` | Name of the reward
`counter` | How many times the reward has been redeemed
`userCounter` | How many times the user has redeemed the reward
`rawInput` | The text a user entered if input was required
`rawInputEscaped` | The text a user entered but escaped
`input<x>` | Single words from the `rawInput` using spaces as delimiters, this will populate consecutive variables starting at `input0` 
`rewardCost` | The channel point cost of the redeemed reward <span style="color:blue">*(0.15+)*</span>
`rewardPrompt` | The verbiage shown on the channel point description <span style="color:blue">*(0.15+)*</span>
***

### [Commercials](/en/Twitch/Commercials)
| Variable | Description |
|---------:|-------------|
| `adLength` | The length of the ad in seconds
| `adScheduled` | If this ad was a scheduled ad (`True`/`False`)


***













### [Stream Update](/en/Events/Stream-Update)

Variable | Description
---------:|------------
`status` | Stream's current Title
`gameUpdate` | Boolean value denoting the Game category changed
`statusUpdate` | Boolean value denoting the stream Title changed
`gameId` | Stream's current game category ID
`gameName` | Stream's current game name
`oldStatus` | Previous stream status
`oldGameId` | Previous game category ID
`oldGameName` | Previous game name
`gameBoxArt` | URL for current game boxart image <span style="color:blue">*(0.15+)*</span>
`oldGameBoxArt` | URL for previous game boxart image <span style="color:blue">*(0.15+)*</span>

### [Polls](/en/Twitch/Polls)

| Variable | Description |
|      ---:|-------------|
| `poll.Id` | Twitch's ID for the poll |
| `poll.StartedAt` | When the poll was started |
| `poll.Title` | The title of the poll |
| `poll.Duration` | How long the poll will run for, in seconds |
| `poll.DurationRemaining` | How much longer the poll has left, in seconds |
| `poll.choices.count` | The number of choices |

#### Choices available

| Variable | Description |
|      ---:|-------------|
| `poll.choice#.title` | The title of the poll choice |
| `poll.choice#.votes` | Number of regular votes for the choice |
| `poll.choice#.bitVotes` | Number of bit based votes for the choice |
| `poll.choice#.rewardVotes` | Number of reward based votes for the choice |
| `poll.choice#.totalVotes`| Total number of votes for the choice |

Replace the # in choice# with 0 to 4, depending how many choices there are, to get the choice entry

| Variable | Description |
|      ---:|-------------|
| `poll.votes` | Total number of regular votes |
| `poll.bitVotes` | Total number of bit based votes |
| `poll.rewardVotes` | Total number of reward based votes |
| `poll.totalVotes` | Overall total number of votes |

The above variables are available for all poll actions

`poll.EndedAt` is also available for the completed action

#### Poll Ended

| Value | Description |
|   ---:|-------------|
| `poll.winningIndex` | The index of the winning choice, from 0 to 4 |
| `poll.winningChoice.id` | The ID of the winning choice |
| `poll.winningChoice.title` | The title of the winning choice |
| `poll.winningChoice.votes` | Number of regular votes |
| `poll.winningChoice.bitVotes` | Number of bit based votes |
| `poll.winningChoice.rewardVotes` | Number of channel point based votes |
| `poll.winningChoice.totalVotes` | Total number of votes for the choice |
| `poll._json` | JSON string of complete event information that can be parsed

- [Polls](/Twitch/Polls)
{.links-list}

### [Predictions](/en/Twitch/Predictions)

| Value | Description |
|   ---:|-------------|
| `prediction.winningIndex` | Either a 0 or 1 depending on which outcome was chosen as the winner |
| `prediction.winningOutcome.id` | The ID of the winning outcome |
| `prediction.winningOutcome.title` | The title of the winning outcome |
| `prediction.winningOutcome.users` | How many users voted for this prediction |
| `prediction.winningOutcome.points` | The total number of channel points used by users |
| `prediction.winningOutcome.color` | The colour of the winning outcome |
| `prediction._json` | JSON string of complete event information that can be parsed

- [Predictions](/Twitch/Predictions)
{.links-list}

### [Message Deleted](/en/Events/General)

| Value | Description |
|   ---:|-------------|
| `message` | The message that was deleted from chat

### [User Timed Out](/en/Events/General)

| Value | Description |
|   ---:|-------------|
| `duration` | The amount of time the user was timed out for
| `user` | The user that was timed out 

### [User Banned](/en/Events/General)

| Value | Description |
|   ---:|-------------|
| `user` | The user that was banned 
>This will not be populated if the user has never been present in chat
{.is-info}

### [Announcement](/en/Twitch/Announcement)

| Value | Description |
|   ---:|-------------|
| `announceColor` | The color of the announcement, `DEFAULT`, `BLUE`, `RED`, `ORANGE`, `PURPLE`
| `message` | The announcement message
| `messageStripped` | The announcement message without emotes
| `emoteCount` | The number of emotes in the message
| `emotes` | The emotes in the message, this is a List<> object
| `badgeCount` | The number of badges for the user making the announcement
| `badged` | The badges for the user making the announcement, this is a List<> object

> This also contains the user's picked color, and user's months subscribed
{.is-info}

***

## YouTube

# {.tabset}

## Broadcast Started

| Variable | Description |
|  ---:|:--- |
| `title` | The title of the broadcast |
| `description` | The description of the broadcast |
| `publishedAt` | The time the broadcast was published at |
| `broadcastId` | The id of the broadcast |

## Broadcast Ended

No variables

## Message

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the message |
| `message` | The message sent to the chat |
| `publishedAt` | The time the message was published at |

## User Banned

| Variable | Description |
|  ---:|:--- |
| `banType` | The type of ban |
| `banDuration` | The duration of the ban |

## Super Chat

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the super chat event |
| `message` | The message of the super chat event |
| `publishedAt` | The time the super chat event was published at |
| `tier` | The tier for the paid message |
| `amount` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user. |
| `microAmount` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000. |
| `currencyCode` | The currency in which the purchase was made. The value is an ISO 4217 currency code. |

## Super Sticker

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the super sticker event |
| `publishedAt` | The time the super sticker event was published at |
| `tier` | The tier for the paid message |
| `amount` | A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user. |
| `microAmount` | The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000. |
| `currencyCode` | The currency in which the purchase was made. The value is an ISO 4217 currency code. |
| `stickerId` | A unique ID that identifies the sticker image. |
| `stickerAltText` | A text string that describes the sticker. |
| `stickerLanguage` | The language of the `stickerAltText` |

## Sponsor

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the sponsor event |
| `publishedAt` | The time the sponsor event was published at |
| `isUpgrade` | Indicates whether the viewer just upgraded from a lower level |
| `levelName` | The name of the Level at which the viewer is a member |

## Member Milestone

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the member milestone event |
| `publishedAt` | The time the member milestone event was published at |
| `months` | The total amount of months (rounded up) the viewer has been a member |
| `levelName` | The name of the Level at which the viewer is a member. |
| `message` | The message associated with the member milestone event |

## Sponsor Only Mode Started

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the sponsor only mode started event |
| `publishedAt` | The time the sponsor only mode event was published at |

## Sponsor Only Mode Ended

| Variable | Description |
|  ---:|:--- |
| `messageId` | The id of the sponsor only mode ended sticker event |
| `publishedAt` | The time the sponsor only mode ended event was published at |

## Membership Gifting

| Variable | Description |
|  ---:|:--- |
| `id` | The title of the broadcast |
| `count` | The description of the broadcast |
| `tier` | The time the broadcast was published at |

## Gift Membership Received

| Variable | Description |
|  ---:|:--- |
| `id` | The id of the membership gifting event |
| `tier` | The tier the gifted user received |
| `gifterUser` | The display name of the user who received the gifted membership |
| `gifterUserName` | The user name of the user who received the gifted membership |
| `gifterUserId` | The id of the user who received the gifted membership |
| `gifterUserType` | The type of user who received the gifted membership |

## Statistics Updated

This event is fired whenever any of the values below change.

| Variable | Description |
|  ---:|:--- |
| `likeCount` | The number of likes the broadcast has |
| `dislikeCount` | The number of dislikes the broadcast has |
| `viewCount` | The number of viewers the broadcast has had |
| `commentCount` | The number of comments added to the broadcast |
| `favoriteCount` | How many times the broadcast has been favorited |

## Broadcast Update

This event is fired whenever any of the values below change.

| Variable | Description |
|  ---:|:--- |
| `id` | The id of the broadcast |
| `title` | The title of the broadcast |
| `description` |The description of the broadcast |
| `privacy` | The privacy setting of the broadcast |

***

# Integrations

# {.tabset}
## [Stream Elements](en/Settings/StreamElements)

### Donation

Variable | Description
---------:|------------
`tipUsername` | Username of the user as provided by StreamElements
`tipAvatar` | Avatar of the user
`tipAmount` | The amount of the tip
`tipCurrency` | 3 letter currency code
`tipMessage` | Any tip message the user included
`isTest` | Boolean value indicating the tip was a test |  `True`/`False` 

### Merchandise

Variable | Description
---------:|------------
`merchUsername` | Username of the user as provided by StreamElements
`merchAvatar` | Avatar of the user
`merchAmount` | The amount of the purchase
`merchCurrency` | 3 letter currency code
`merchMessage` | Any message the user included
`merchQuantity` | The total number of items purchased
`merchItems` | The number of distinct items purchased

`merchItem#.name` | Name of the item purchased, where # is the index of the item (0 based)
`merchItem#.price` | Price of the item purchased, where # is the index of the item (0 based)
`merchItem#.quantity` | How many of the item was purchased, where # is the index of the item (0 based)


## [StreamLabs](/en/Settings/Streamlabs)

### Donations

Variable | Description
---------:|------------
`donationFrom` | Who the donation was from, as the user filled out
`donationAmount` | the amount of the donation
`donationCurrency` | 3 letter currency code
`donationFormattedAmount` | The donation amount with the currency symbol
`donationMessage` | Any donation message the user may have included
`isTest` | Boolean value indicating if the donation was a test |  `True`/`False` 


### Merchandise

Variable | Description
---------:|------------
`merchandiseFrom` | Who purchased a product
`merchandiseMessage` | Any message the user attached to the purchase
`merchandiseProduct` | The product that was purchased
`merchandiseImageUrl` | URL to the image of the product
`merchandiseImageEscaped` | URL to the image of the product with escaped characters
`isTest` | Boolean value indicating if the purchase was a test |  `True`/`False` 

## [TipeeeStream](/en/Integrations/TipeeeStream)

### Donation

Variable | Description
---------:|------------
`tipUsername` | Who the donation was from, as the user filled out
`tipAvatar` | Avatar of the user
`tipAmount` | The amount of the tip (decimal value)
`tipCurrency` | 3 letter curency code
`tipMessage` | Any donation message the user may have included

## [TreatStream](/en/Integrations/TreatStream)

### Treat Event
 
Details coming soon

## [Hype Rate](/en/Integrations/HypeRate-io)

### Heart Rate Event
 
| Variable | Description |
|   ---:|-------------|
| `measuredAt` | Time the measurement was taken |
| `heartRate` | Heart Rate value |

## [Pulsoid](/en/Integrations/Pulsoid)

### Heart Rate Event

| Variable | Description |
|   ---:|-------------|
| `measuredAt` | Time the measurement was taken |
| `heartRate` | Heart Rate value |

## [Donor Drive](/en/Integrations/DonorDrive)

### Donation
 
Details coming soon

### Profile Update
 
Details coming soon

## [Kofi](/en/Integrations/Kofi)

### Donation
 
This event is triggered when a donation happens through Kofi

| Variable | Description |
|   ---:|-------------|
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The amount donated |
| `currency` | The currency of the donation |

### Subscription
 
This event is triggered when a donation happens through Kofi

| Variable | Description |
|   ---:|-------------|
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The amount donated |
| `currency` | The currency of the donation |

### Resubscription
 
This event is triggered when a resubscription happens through Kofi

| Variable | Description |
|   ---:|-------------|
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The subscription amount |
| `currency` | The currency of the subscription |
| `tier` | The tier of the subscription |

### Shop Purchase
 
This event is triggered when a shop purchase happens through Kofi

| Variable | Description |
|   ---:|-------------|
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The amount of the purchase |
| `currency` | The currency of the purchase |
| `itemCount` | The currency of the donation |
| `item#` | The id of the item purchased, where # is the index of the item |

### Commissions
 
This event is triggered when a commission is purchased on Kofi

| Variable | Description |
|   ---:|-------------|
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The commission amount |
| `currency` | The currency of the commission |

## [Patreon](/en/Integrations/Patreon)

### Follow Created
 
Details coming soon

### Follow Deleted
 
Details coming soon

### Pledge Created
 
Details coming soon

### Pledge Updated
 
Details coming soon

### Pledge Deleted
 
Details coming soon

## [streamer.bot](/en/Integrations/Streamer-bot)

### Deck Button
 
#### Variables
| Variable | Description |
|      ---:|-------------|
| `streamerbotUserId` | The streamer.bot user ID |
| `streamerbotUserDiscordId` | The discord ID of the redeemer |
| `streamerbotUserUsername` | The username of the redeemer |
| | Your own inputted variables on the decks |

# App Features

# {.tabset}
## Pyramids

| Value | Description |
|   ---:|-------------|
| `totalPyramids` | The total number of pyramids this user has made
| `pyramidEmote` | The emote that completed the pyramid
| `pyramidWidth` | The pyramid width




## [Present Viewers](/en/Events/General)

| Value | Description |
|   ---:|-------------|
| `isLive` |Boolean for current streaming status |  `True`/`False` 

| `isTest` |Boolean for if this is demo data or not |  `True`/`False` 

| `users` | A Dictionary list of usernames present in IRC chat


### User Dictionary
>
> Each user entry will contain the following data:
> 
> 
> | Value | Description | Notes
> |   ---:|-------------|
> | `id` | The Numeric ID of this user
> | `userName` | The user name of this user
> | `display` | The display name of this user
> | `role` | The role of the user | 1=`Viewer`, 2=`VIP`, 3=`Moderator`, 4=`Broadcaster`
> | `isSubscribed` | Boolean for this users subscription status |  `True`/`False` 

{.is-info}


***
### Live Variables 

If `isLive` is `True` the following variables will also be populated on each tick of the event:

| Value | Description |
|   ---:|-------------|
| `title` | The current stream title
| `gameID` | The ID of the category you are streaming
| `gameName` | The name of the category you are streaming
| `viewerCount` | Viewer count at the time of the tick
| `startedAt` | The time stamp when you started streaming

## [File/Folder Watcher](/en/Settings#filefolder-watcher)

| Variable | Description | Notes
|      ---:|-------------|---
| `changeType` | The type of change | `Changed`, `Created`, `Deleted`
| `fullPath` | The full path to the file |
| `fileName` | The file name with extension |
| `name` | The file name without the extendion |
| `empty` | A boolean value indicating if the file is empty |

If you have `As JSON` ticked, it will add all root elements as arguments.

If `As JSON` is not ticked, it will add the following variables:

| Variable | Description |
|      ---:|-------------|
| `lineCount` | The number of lines in the file |
| `line#` | The line of the file, replace # with the line number you want |
| `lineEscaped#` | The line of the file URL encoded, replace # with the line number you want |

## [Sub Counter](/en/Settings#sub-counter)

| Variable | Description |
|      ---:|-------------|
| `subCounter` | The number of subs SB has been able to count |
| `rollover` | The target number for the sub-counter - triggers the specified action and resets the counter |
| `rolloverCount` | The number of times the rollover target has been reached |

## [Quotes](/en/Settings/Quotes)
When using the built in `!quote` command the following variables will be available to you
| Variable | Description |
|   ---:|-------------|
`quote` | The quote content
`quoteID` | The quote ID number
`quoteUser` | The user that added the quote,
`quoteGame` | The game the broadcaster was playing at the time
`quoteTime` | The date it was logged

## [Voice Control](/en/Voice-Control)

Any action triggered by Voice Control will have access to the following arguments that can be used in other Sub-Actions or C# code

Variable | Description
---------:|------------
`spokenText` | The full spoken phrase detected, *including the trigger phrase* 
`spokenTextConfidence` | Voice Recognition confidence raw value
`spokenTextConfidencePercent` | Confidence value as a percentage
`altPhraseText#` | 
`altPhraseConfidence#` | 
`altPhraseConfidencePercent#` | 
`spokenTextInput` | Detected spoken phrase with trigger command stripped <span style="color:blue">*(0.15+)*</span> <br>(Only works with `Start` based commands)
`spokenCommand` | Detected Trigger command <span style="color:blue">*(0.15+)*</span>

***

# Commands

| Variable | Description | Notes
|   ---:|-------------|---
| `command` | The command that was used |
| `commandID` | The ID of the command that was used | <span style="color:blue">*(0.18+)*</span>
| `rawInput` | The message entered, if the command was a Starts With, this will be removed |
| `rawInputEscaped` | The message escaped |
| `rawInputUrlEncoded` | The message URL encoded |
| `input#` | The # word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on |
| `inputEscaped#` | The indexed word escaped |
| `inputUrlEncoded#` | The indexed word URL encoded |
|`message` | The message typed in chat | (unverified)
|`role` | What role the user has `(1-4)` | 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
|`isSubscribed` | Is user subscribed
| `counter` | A running total of how many times a command has been run since application launch (if `Persisted` is checked, the total will be saved to settings.dat and read in at launch) |
| `userCounter` | A running total of how many times a command has been run by this chat user since application launch (if `UserPersisted` is checked, the total will be saved to settings.dat and read in at launch) |

If a cooldown action is set, and the command is in cooldown, the following variables will be the only ones available.

| Variable | Description |
|   ---:|-------------|
| `command` | The command that was used |
| `cooldownLeft` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left |
| `globalCooldownLeft` | How many seconds are left for the global cooldown of the command |
| `userCooldownLeft` | How many seconds are left for the user cooldown of the command |



# Sub-Actions

Variables that various [Sub-Actions](/Sub-Actions) can add to the argument stack

## [Get User Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target)

Variable | Description
---------:|------------
`targetUser` | Display name of the target user
`targetUserName` | User name of the target user
`targetUserId` | User Id of the target user
`targetDescription` | The user's channel description
`targetDescriptionEscaped` | The user's channel description but URL encoded
`targetUserProfileImageUrl` | link to the 300x300 px PNG version of a user's twitch profile image
`targetUserProfileImageUrlEscaped` | The url to the user's profile image URL encoded
`targetUserType` | The type of user, `affiliate`, `partner` or empty for regular user
`targetIsAffiliate` | A boolean value indicating if the user is an affiliate
`targetIsPartner` | A boolean value indicating if the user is a partner
`targetIsSubscribed` | A boolean value indicating if the user is currently subscribed
`targetIsModerator` | A boolean value indicating if the user is a moderator
`targetIsVip` | A boolean value indicating if the user is a VIP
`game` | The user's current game category
`gameId` | The numeric id of the game category
`createdAt` | Datetime of when the account was created (v0.1.4+)
`accountAge` | Age of the account in seconds (v0.1.4+)

## [Get Follow Age](en/Sub-Actions/Twitch/Get-Follow-Age-for-Target)

> Note if you are testing any of the Follow age variables, it will not work from the broadcaster account as you are unable to follow yourself. 
Test it from the bot acocunt or any other Twitch! user
{.is-info}


Variable | Description
---------:|------------
`followDate`| The date the user followed
`followAgeLong` | How long the user has been following in a long format, 1 year, 10 months, 5 days, etc
`followAgeShort` | How long the user has been following in a short format, 1y, 10m, 5d, 22h, 3m, 25s
`followAgeDays` | The total number of days the user has been following
`followAgeMinutes` | The total number of minutes the user has been following
`followAgeSeconds` | The total number of seconds the user has been following
`followUser` | The users display name
`followUserName` | The user's login name
`followUserId` | The user's twitch id

## [Get Random Number](/en/Sub-Actions/Get-Random-Number)

If you pick a random number between 2 values, you will get the following variables

Variable | Description
---------:|------------
`randomNumber` | Random number

If you pick next float, you will get the following

Variable | Description
---------:|------------
`randomFloat` | A floating point number between 0 and 1
`randomPercent` | The floating point number represented as a percentage

## [Get Current Scene](/en/Sub-Actions/OBS/Get-Current-Scene)

Variable|Description
---|---
`currentScene` | the name of the currently active scene at the time of execution

## [Read Lines From File](/en/Sub-Actions/File#read-lines-from-file)

Variable | Description
---------:|------------
`lineCount` | The number of lines read from the file
`line#` | The line number from the file, replace `#` with the line number, starting from **0**

## [Read Random Line](/en/Sub-Actions/File#read-random-line-from-file)

Variable | Description
---------:|------------
`randomLine#` | Reads a random line from a given source file, the first will have no number, then 1, 2, 3 and so on for each concurrent use within the same action. i.e. `%randomLine%`, `randomLine1`, `randomLine2`

## [OBS Take Screenshot](/en/Sub-Actions/OBS/Take-Screenshot)

Variable | Description
---------:|------------
`screenshotFile` | The full path to the screenshot that was taken
`filedatetime` | Date Time varible that can be used for file name, `yyyyMMdd.hhmmss` formatting

## [Pick Color](/en/Sub-Actions/Pick-Color)

> `var` needs to be changed with the variable you have putted in the `Variable Name` box
{.is-info}

Variable | Description
---------:|------------
| `var.color.a` | The alpha value |
| `var.color.r` | The red value |
| `var.color.g` | The green value |
| `var.color.b` | The blue value |
| `var.html` | The html color code |
| `var.htmlalpha` | The html color code with alpha value |
| `var.obs` | The color as an OBS ABGR value |

## [Get Commands](/en/Sub-Actions/Commands#get-commands)
This subaction populates 2 variables with the custom name you specify, one as a string and one as a list
Variable | Description
---------:|------------
| `<variableName>` | Comma separated string containing all commands matching criteria specified in the sub-action |
| `<variableName.List` | List object for C# containing all commands matching criteria specified in the sub-action |

## [Get Command State](/en/Sub-Actions/Commands#get-command-state)

Variable | Description
---------:|------------
| `commandState` | Boolean for command enabled state | `True`/`False` 

## [Get Command Group State](/en/Sub-Actions/Commands#get-command-group-state)

Variable | Description
---------:|------------
| `commandGroupState` | Boolean for command group enabled state | `True`/`False` 
| `commandsEnabled` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are enabled |
| `commandsDisabled` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are disabled |

## [Get Action State](/en/Sub-Actions/Actions#get-action-state)

Variable | Description
---------:|------------
| `actionState` | Boolean for action enabled state | `True`/`False` 

## [Get Action Group State](/en/Sub-Actions/Actions#get-action-group-state)

Variable | Description
---------:|------------
| `actionGroupState` | Boolean for action group enabled state | `True`/`False` 
| `actionsEnabled` | A list of action IDs, of actions that are enabled |
| `actionsDisabled` | A list of action IDs, of commands that are disabled |


## [OBS Raw](/en/Sub-Actions/OBS/Raw)

OBS RAW allows bi-directional communication to and from OBS via the Websocket Protocol

> Protocols supported will depend on which version of Websocket you have installed, current references can be found here that lists all possible commands and the variables those commands expect
https://github.com/Palakis/obs-websocket/blob/4.x-current/docs/generated/protocol.md
{.is-info}

If OBS returns any information, Streamer.bot will store the entire JSON responce as an argument that can be queried by its Key values in the format 

`obsRaw.{path}`
So for example if you needed the `status` variable from OBS it would be under `obsRaw.status`

Exact variables available will depend on the request sent but as an example, if a `GetSceneItemProperties` request was sent, all the following data should be available

![obs-raw-example.png](/obs-raw-example.png)

At a minimum, the variable `obsRaw._json` should be populated with a json string of the entire response from OBS.


## Get Scene Item Properties

This action populates all available variables for a given OBS source
all variables will be in the format `props.***` 

e.g `props.visible` will return `True` if the source is showing. This can then be used in an IF statement in the same action for example. 

***

## Timeout User

Variable | Description
---------:|------------
`timedoutUser0` | The username of the user currently timed out by Streamerbot action
`timedoutUserName0` | The Display of the user currently timed out by Streamerbot action

***



***



> *More to be added soon
{.is-info}