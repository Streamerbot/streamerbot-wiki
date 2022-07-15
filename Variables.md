---
title: Variables
description: Reference of all variables/arguments that may be available in Streamer.bot events and sub-actions
published: true
date: 2022-07-15T17:58:43.674Z
tags: variables, arguments
editor: markdown
dateCreated: 2021-08-25T21:34:50.460Z
---

# Overview

All [events](/en/Events) in Streamer.bot will generate an **argument stack** specific to that event source, providing variable data to the action (and subsequent [sub-actions](/en/Sub-Actions)) being called.

Most events will always include all generic arguments in addition to their own documented variables. Any exceptions will be listed on the page detailing that function.

**This list is not exhaustive and some variables may work with sub-actions / events even though they do not specifically state compatibility.**

> **NOTE**
> If an event is not documented, you can always use [Log All Arguments](/Sub-Actions/Code/Execute-CSharp-Code/Examples/Log-All-Arguments) in a sub-action to see all variables available to you.
{.is-info}


# Usage

Variables can be used in most [sub-action](/en/Sub-Actions) text inputs.

To use a variable from the current argument stack, wrap the variable name with a `%` symbol, e.g. `%userName%`

## Tips

- Arguments only persist until the called action finishes execution and can not be referenced by any other action
	- If you want to share variables across multiple actions you can write them out to a [Global](/en/Sub-Actions/Logic/Global-Variables) variable{.small}
- Variables are added onto the argument stack during execution of each sub-action
  - If you are testing and a variable seems to be missing, ensure you are testing at the right point of execution{.small}
- You do not need to wrap variable names with `%` within logic statements like `If` and `Global`
  - This was required in older versions of Streamer.bot{.small}
  - Wrapped variable names will still work as normal in this context{.small}


## Formatting
Variables can be formatted inline using standard C# notation

For example, to format a numeric veriable `%tipAmount%` as a currency with 2 decimal places, we can use the following syntax: `%tipAmount:c2%`

Similarly, `%time%` can formatted in short notation with AM/PM using the following syntax: `%time:t%`

Further information on valid formatting modifiers can be found [here](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings)


# Variable Sources
- [<i class="mdi mdi-variable-box primary--text"></i> **Generic Variables *Available to most triggers automatically***](/en/Variables/Generic)
- [<i class="mdi mdi-creation primary--text"></i> **Events *All events and their associated variables***](/en/Events)
- [<i class="mdi mdi-lightning-bolt-outline primary--text"></i> **Sub-Actions *Some sub-actions will also generate variables***](/en/Sub-Actions)
- [<i class="mdi mdi-comment-alert primary--text"></i> **Commands *Variables from triggered chat commands***](/en/Commands)
- [<i class="mdi mdi-triangle-outline primary--text"></i> **Pyramids *Variables related to chat pyramids***](/en/Settings/Pyramids)
- [<i class="mdi mdi-file-document-multiple primary--text"></i> **File/Folder Watcher *Variables from monitored files & folders***](/en/Settings/File-Folder-Watcher)
- [<i class="mdi mdi-account-heart primary--text"></i> **Sub Counter *Variables from sub counter settings***](/en/Settings/Sub-Counter)
- [<i class="mdi mdi-comment-quote primary--text"></i> **Quotes *Variables from the built-in `!quote` command***](/en/Settings/Quotes)
- [<i class="mdi mdi-account-voice primary--text"></i> **Voice Control *Variables from all Voice Control actions***](/en/Settings/Voice-Control)
- [<i class="mdi mdi-twitch text--twitch"></i> **Broadcaster *Variables related to the Twitch broadcaster account*  *v0.1.5 - 0.1.7*{.version-badge}**](/en/Variables/Broadcaster)
{.btn-grid .my-5}

> **WORK IN PROGRESS**
> wee woo wee woo wee woo
> everything below this is getting removed
{.is-warning}

# App Features

## Pyramids

| Value | Description |
|   ---:|-------------|
| `totalPyramids` | The total number of pyramids this user has made
| `pyramidEmote` | The emote that completed the pyramid
| `pyramidWidth` | The pyramid width


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
|---------:|:------------|
| `lineCount` | The number of lines in the file |
| `line#` | The line of the file, replace # with the line number you want |
| `lineEscaped#` | The line of the file URL encoded, replace # with the line number you want |

## [Sub Counter](/en/Settings#sub-counter)

| Variable | Description |
|---------:|:------------|
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

| Variable | Description |
|---------:|:------------|
`spokenText` | The full spoken phrase detected, *including the trigger phrase*
`spokenTextConfidence` | Voice Recognition confidence raw value
`spokenTextConfidencePercent` | Confidence value as a percentage
`altPhraseText#` |
`altPhraseConfidence#` |
`altPhraseConfidencePercent#` |
`spokenTextInput` | Detected spoken phrase with trigger command stripped *v0.1.5+*{.version-badge} <br>(Only works with `Start` based commands)
`spokenCommand` | Detected Trigger command *v0.1.5+*{.version-badge}


# Commands

Commands are platform agnostic and will trigger when a matching phrase is typed into chat / whisper

> Command events can trigger chat events at the same time but the argument stack for each are completely separate.
{.is-warning}


| Variable | Description | Notes
|   ---:|-------------|---
| `command` | The command that was used |
| `commandID` | The ID of the command that was used | *v0.1.8+*{.version-badge}
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
Some [Sub-Actions](/Sub-Actions) will also add variables to the argument stack{.subtitle}

## [Get User Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target)

| Variable | Description |
|---------:|:------------|
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


| Variable | Description |
|---------:|:------------|
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

| Variable | Description |
|---------:|:------------|
`randomNumber` | Random number

If you pick next float, you will get the following

| Variable | Description |
|---------:|:------------|
`randomFloat` | A floating point number between 0 and 1
`randomPercent` | The floating point number represented as a percentage

## [Get Current Scene](/en/Sub-Actions/OBS/Get-Current-Scene)

Variable|Description
---|---
`currentScene` | the name of the currently active scene at the time of execution

## [Read Lines From File](/en/Sub-Actions/File#read-lines-from-file)

| Variable | Description |
|---------:|:------------|
`lineCount` | The number of lines read from the file
`line#` | The line number from the file, replace `#` with the line number, starting from **0**

## [Read Random Line](/en/Sub-Actions/File#read-random-line-from-file)

| Variable | Description |
|---------:|:------------|
`randomLine#` | Reads a random line from a given source file, the first will have no number, then 1, 2, 3 and so on for each concurrent use within the same action. i.e. `%randomLine%`, `randomLine1`, `randomLine2`

## [OBS Take Screenshot](/en/Sub-Actions/OBS/Take-Screenshot)

| Variable | Description |
|---------:|:------------|
`screenshotFile` | The full path to the screenshot that was taken
`filedatetime` | Date Time varible that can be used for file name, `yyyyMMdd.hhmmss` formatting

## [Pick Color](/en/Sub-Actions/Pick-Color)

> `var` needs to be changed with the variable you have putted in the `Variable Name` box
{.is-info}

| Variable | Description |
|---------:|:------------|
| `var.color.a` | The alpha value |
| `var.color.r` | The red value |
| `var.color.g` | The green value |
| `var.color.b` | The blue value |
| `var.html` | The html color code |
| `var.htmlalpha` | The html color code with alpha value |
| `var.obs` | The color as an OBS ABGR value |

## [Get Commands](/en/Sub-Actions/Commands#get-commands)
This subaction populates 2 variables with the custom name you specify, one as a string and one as a list
| Variable | Description |
|---------:|:------------|
| `<variableName>` | Comma separated string containing all commands matching criteria specified in the sub-action |
| `<variableName.List` | List object for C# containing all commands matching criteria specified in the sub-action |

## [Get Command State](/en/Sub-Actions/Commands#get-command-state)

| Variable | Description |
|---------:|:------------|
| `commandState` | Boolean for command enabled state | `True`/`False`

## [Get Command Group State](/en/Sub-Actions/Commands#get-command-group-state)

| Variable | Description |
|---------:|:------------|
| `commandGroupState` | Boolean for command group enabled state | `True`/`False`
| `commandsEnabled` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are enabled |
| `commandsDisabled` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are disabled |

## [Get Action State](/en/Sub-Actions/Actions#get-action-state)

| Variable | Description |
|---------:|:------------|
| `actionState` | Boolean for action enabled state | `True`/`False`

## [Get Action Group State](/en/Sub-Actions/Actions#get-action-group-state)

| Variable | Description |
|---------:|:------------|
| `actionGroupState` | Boolean for action group enabled state | `True`/`False`
| `actionsEnabled` | A list of action IDs, of actions that are enabled |
| `actionsDisabled` | A list of action IDs, of commands that are disabled |

## Timeout User

| Variable | Description |
|---------:|:------------|
`timedoutUser0` | The username of the user currently timed out by Streamerbot action
`timedoutUserName0` | The Display of the user currently timed out by Streamerbot action