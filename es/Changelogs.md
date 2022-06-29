---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2022-01-15T20:32:12.180Z
tags: 
editor: markdown
dateCreated: 2022-01-15T20:22:49.028Z
---

# Streamer.bot v0.1.7 (Actual)
* **Corregido:** la subacción Get/Set Action State tenía un título incorrecto en el cuadro de diálogo
* **Corregido:** el estado del búfer de reproducción de OBS estaba usando datos incorrectos, debería funcionar correctamente ahora
* **Corregido:** corrige el error tipográfico en Logic si
* **Corregido:** los comandos de control de voz se eliminarán correctamente ahora si no está activo
* **Corregido:** Establecer fuente de medios debería establecer un archivo local correctamente ahora
* **Corregido:** /me ya no causa problemas con el análisis de emoticonos de Twitch
* **Corregido:** las fallas de resolución de DNS de 7TV ya no deberían causar un bloqueo de inicio
* **Corregido:** GetClips debería funcionar correctamente ahora al especificar rangos de fechas


> Además de poder especificar intervalos de fechas/recuentos para los clips, ya no se devuelven del más reciente al más antiguo, se devuelven del más antiguo al más reciente, ya que así es como la API de Twitch devuelve los datos. No hay ningún mecanismo en la API para cambiar el orden de clasificación. Las entradas de Wiki se actualizarán para indicar esto.
{.is-info}

* **Actualización:** la acción de enfriamiento del comando ahora se aplica a cualquier tipo de comando, en lugar de solo exacto/inicio
* **Actualización:** FetchURL ahora reconoce el tipo, la variable en la que se coloca el resultado intentará hacer coincidir su contenido con el tipo adecuado, esta es una actualización intermedia hasta que se pueda hacer más. Si desea un control explícito, use C# para obtener datos
* **Actualización:** biblioteca Newtonsoft.Json actualizada a 13.0.1


# Streamer.bot v0.1.6
* **Fixed:** Changing category would cause a crash
* **Fixed:** Clearing chat caused the Banned event to fire
* **Fixed:** Multi-word commands are now checked correctly
* **Fixed:** Custom websocket server would crash when the connection was terminated

# Streamer.bot v0.1.5

* **Fixed:** Typos
* **Fixed:** Regression in Perform Command, variables were not being parsed
* **Fixed:** Better handling of OBS events, and issues surrounding editing
* **Fixed:** Better handling of OBS/SLOBS sub-actions where a scene is empty, signifying the source exists in any scene
* **Fixed:** Anonymous cheers could cause a crash with credits
* **Fixed:** Some underlying issues with Streamlabs/Streamelements sockets
* **Fixed:** Add error handling when importing actions, should no longer crash in the event something is malformed
* **Fixed:** Handle WASAPI init errors on playback, specifically if its unable to initialize the device
* **Fixed:** Some additional error handling in websocket server/client dialogs
* **Fixed:** Rare scenario where fetching mod/vip lists internally could cause a crash
* **Fixed:** Handle data issues with SLOBS not adhering to its on JSON structures
* **Fixed:** Grouping in OBS Events was not being handled properly (typo)
* **Fixed:** Custom WebsocketServer message event was emitting the wrong type of event internally
* **Fixed:** GetCredits method was putting Hype Train conductors in the wrong field
* **Fixed:** Twitch Slow mode sub-action was not being deserialized properly
* **Fixed:** Read Lines from File and Read Random Line from File sub-actions, input validation input was not working correctly
* **Fixed:** Creating/editing reward sub-actions when there are none could cause a potential crash
* **Fixed:** Fix culture parsing of decimals for streamlabs and stream elements testing of donations, decimals should work for all cultures now
* **Fixed:** Potential crash in some sub-actions and empty scenes
* **Fixed:** Drag/drop of sub-action was not properly marking cached info as dirty
* **Fixed:** Voice control UI was not selecting the saved input device on startup
* **Fixed:** Issues with Twitch dropping connection, this maybe an on going fix, trying to refine why this behaviour is happening.  This manifests as if the bot stops reacting to most Twitch actions.
* **Fixed:** Actions were not being flagged as dirty when using drag/drop to re-organize sub-actions, making it look like they were not being saved
* **Fixed:** Streamlabs donation events were being ignored, they should go through now
* **Fixed:** Resuming a queue should now correctly fire off any actions that were in the queue
* **Fixed:** Masimum values for max redeems per user/per stream are set to correct maximums now, should no longer cause a crash
* **Fixed:** Data type mismatch when creating Stream Markers (oops)
* **Fixed:** Exporting actions with a queue did not preserve is the queue was blocking
* **Fixed:** Importing actions did not correctly show blocking/non-blocking queue info (visual only)
* **Fixed:** Custom websocket server firing incorrect actions
* **Update:** [Delay](#delay-sub-action) sub-action can now accept variables
* **Update:** Twitch Slow Mode sub-action (and C# method) has been updated to allow specifiying the delay time
* **Update:** Update [Twitch Clip C# Methods](#twitch-clip-c-methods) related methods, see section for more details
* **Update:** %s are auto removed for the variable in the LogicIf dialog
* **Update:** Add Insert and Delete as usable keys for Hot Keys and Keyboard Press
* **Update:** [Set Reward Cost](#set-reward-cost) sub-action can now accept variables, and give an operator option to add, subtract, multiply or divide the value
* **Update:** [Set Argument](#set-argument) sub-action has been updated with full parsing support for its value, and the increment option removed, see section for more details
* **Update:** New way to [pick actions](#new-way-to-pick-actions) for events!
* **Update:** Added `%rewardCost%` and `%rewardPrompt%` to the variables for reward redemptions
* **Update:** The action list in the action sub-action is now sorted alphabetically
* **Update:** Action lists returned by the HTTP server and Websocket GetActions requests are now sorted alphabetically
* **Update:** Timed Actions have been decoupled from the Twitch connection, they will now start on application start
* **Update:** Resolution for Timed Actions has been lowered to 1s from 53, this is tenetive and needs testing internally
* **Update:** Add game box art (`%gameBoxArt%` and `%oldGameBoxArt%`) to the stream update event
* **Update:** Global Get/Set sub-actions have been extended to parse the variable name, bringing support for `%variable%` parsing for the variable name itself
* **Update:** Setting auto reset first words cache time to -1 will disable this check on startup
* **Update:** Alter how commands start with check is performed, so a command of `!so` wouldn't trigger on `!socials`
* **New:** New sub-action to set the [OBS Replay Buffer State](#obs-replay-buffer-state), as well as C# methods
* **New:** Added 2 new [C# Methods](#obs-color-helpers) to translate colors to OBS color
* **New:** Added a new [C# Helper Method](#obs-helper-methods) to get a connection index by name
* **New:** New sub-action [Set Reward Title](#set-reward-title), along with a C# method
* **New:** New sub-action [Set Reward Prompt](#set-reward-prompt), along with a C# method
* **New:** New sub-action [Update Reward](#update-reward), where you can set the title, prompt and cost of a reward in one call, along with a C# method
* **New:** Added ability to double click to edit Websocket Servers and Clients
* **New:** Added new variable `%spokenTextInput%` to Speech To Text events for Commands, this is the text spoken without the trigger word, and is only support for Start based commands
* **New:** Added new variable `%spokenCommand%` to Speech to Text events that will contain the command that triggered the event
* **New:** A new Twitch scope will be requested on first start, Commercial Edit
* **New:** New sub-action [OBS Get Scene Item Properties](#obs-get-scene-item-properties) to get the properties of a scene item, as well as a C# method
* **New:** New sub-action [Start Commercial](#start-commercial) to start commercials on your channel, as well as C# methods
* **New:** New sub-action [OBS Set Media Source File](#obs-set-media-source-file) to set the file of an OBS Media Source, as well as C# methods
* **New:** New sub-action [OBS Set Image Source File](#obs-set-image-source-file) to set the file of an OBS Image Source, as well as C# methods
* **New:** Support for [DonorDrive](#donordrive) services! This includes ExtraLife, StackUp and any other charity drives that use DonorDrive.
* **New:** The first [Inline Function](#inline-function) has arrived!
* **New:** Added new keys to [Hot Keys and Keyboard Presses](#new-hot-keys-and-keyboard-presses)
* **New:** Add new [C# Methods](#command-cooldown-methods) to alter the cooldowns of a command
* **New:** New sub-action [Get Commands](#get-commands) to get a list of your commands
* **New:** New sub-action [Run Commercial](#run-commercial) to run a commercial on your channel, as well as a C# method
* **New:** Added option to Gift Subs to ignore those that come from a Gift Bomb, there is also a variable `%fromGiftBomb%` that can be checked
* **New:** With the new way actions are selected, most lists have a new menu item to select the action without needing to edit
* **New:** The user list in the Timeout User sub-action is now sorted alphabetically, and I've updated the control to support auto complete suggestions to help find user names.
* **New:** New sub-action [Get Command State](#get-command-state) to get the state of a command, or command group
* **New:** New sub-action [Get Action State](#get-action-state) to get the state of an action, or action group
* **New:** Added some [new action wide variables](#new-action-wide-variables)
* **New:** New sub-action [TwitchSpeaker Speak](#twitchspeaker-speak) to provide a simpler way to get TwitchSpeaker to speak for you, as well as a C# method
* **New:** 3 new Twitch events can be broadcast across the websocket, message deletion, user timeout and user ban
* **New:** New sub-action **Break** that will halt the action from continuing, mostly used when debugging
* **New:** Added new events for twitch message deletion, user being timed out, and a user being banned

## DonorDrive

You can add either your team, or personal campaign for ExtraLife, StackUp or any other charity that uses DonorDrive, and attach an action to a donation event.

This is not limited to just 1, you can add multiple as well.

More info to be filled in.

## Inline Function

Up until now, the only thing that could be parsed were `%variables%`, I have finally added the first function to this, `$math()$`.

Anywhere there is full parsing, you can now perform math operations, and also use variable within the math function itself.

Here is just a simple example of an action:
* Set Argument `%x%` to `1`, `%x%` is now 1
* Set Argument `%x%` to `$math(%x%+1)$`, incrememnt `%x%` by `1`, `%x%` is now `2`
* Set Argument `%x%` to `$math(%x%^2)$`, set `%x%` to `%x%` to the power of `2`, `%x%` is now `4`
* Set Argument `%x%` to `$math(%x%*16)$`, set `%x%` to `%x%` times `16`, `%x%` is now `64`

A page with the possible usages of the `math` function will be added as well, as it is more then just your basic arithmetic (yes, you can even do derivatives or integrals if you wanted to).

## New Way to Pick Actions

With this update, I've completely removed the mess of dropdowns to select events.  This was slowing down the application with the amount of updates this could generate to keep track of any changes to your actions.

There is now a clickable button that will bring up a dialog with your actions grouped and sorted like they are on the main actions page.  This dialog is very much a WIP, and will evolve over time.

In addition to events, most dialogs where you picked actions (Commands, Channel Reward, Timed Actions, etc) have also received this update.

As an added bonus, most of the lists where you edit these kinds events, now have a new context menu item to be able to change the action without having to go in and edit the command, reward, etc.

## Set Argument

With the addition of the `$math()$` inline function, the **Set Argument** sub-action has been updated to fully support parsing its value, and the Increment option has been removed, as you can now use the math function to do this.

![sub-action-set-argument-002.png](/sub-action-set-argument-002.png)

> A configuration upgrade will happen, converting any Set Argument that is flagged as increment will have its value converted to `$math(Variable+Value)$`, there is the possibility this may not fully work, so it is advised to check any Set Arguments you have that were converted.
{.is-info}

## New Hot Keys and Keyboard Presses

A few new keys were added to be the list of keys usable for Hot Keys and Keyboard Press

* Semi Colon `;:`
* Forward Slash `/?`
* Tilde `~`
* Opening Square Brace `[{`
* Backslash `\|`
* Closing Square Brace `]}`
* Double Quote `"`
* Comma `,<`
* Minus Sign `-_`
* Period `.>`
* Plus Sign `+=`
* Break
* Scroll Lock
* Media Next Track
* Media Previous Track
* Media Stop
* Media Play/Pause
* Media Volume Mute
* Media Volume Down
* Media Volume Up

## Twitch Clip C# Methods

Previously, the C# calls to get Twitch clips, only allowed getting all the clips, leaving it upto you to sort through them afterwards.  If there were many clips for a user, this could take a while to fetch, and as it wsa a paginated call, it was only grabbing 20 at a time leading to further slow down.

The first fix, it now fetches 100 at a time (the maximum allowed per call),  This means, ever paged call takes approximately 800 milliseconds to complete.

The methods for fetching clips have been updated to allow for a count to be specified, and it will only grab that many clips for a user, default sorted newest to oldest.

They have also been updated to specific a date range (start and end date) to look for clips, as well as a day timespan, to specifiy the past 7 days, or the past 30 days, etc.

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

## New Action Wide Variables

If Twitch is connected, actions will have the following five variables available to them

| Variable | Description |
|   ---:|-------------|
| `%broadcastUser%` | The Twitch display name of the broadcast account |
| `%broadcastUserName%` | The Twitch user name of the broadcast account |
| `%broadcastUserId%` | The Twitch user ID of the broadcast account |
| `%broadcastIsAffiliate%` | true/false value indicating if the broadcast account is an affiliate |
| `%broadcastIsPartner%` | true/false value indicating if the broadcast account is a partner |

## New Sub-Actions

### Set Reward Title

Change the Title of an existing reward, this also supports the use of `%variables%`

![sub-action-set-reward-title-001.png](/sub-action-set-reward-title-001.png)

#### New C# Method

```csharp
void UpdateRewardTitle(string rewardId, string title);
```

### Set Reward Prompt

Change the prompt of a reward, this also supports the use of `%variables%`

![sub-action-set-reward-prompt-001.png](/sub-action-set-reward-prompt-001.png)

> There is a bug on Twitch's side with the API call, it is not possible to set the prompt to an empty value once it has been set.  This issue also happens with Twitch's own editing of a reward on the website
{.is-info}

#### New C# Method
```csharp
void UpdateRewardPrompt(string rewardId, string prompt);
```

### Update Reward

Change the title, prompt and/or cost of a reward in 1 sub-action.

![sub-action-reward-update-001.png](/sub-action-reward-update-001.png)

#### New C# Method
```csharp
void UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null);
```

### OBS Replay Buffer State

New sub-action to control the Replay Buffer state, no longer need to use OBS Raw to achieve this

![sub-action-obs-set-replay-buffer-state-001.png](/sub-action-obs-set-replay-buffer-state-001.png)

#### New C# Methods for OBS Replay Buffer State
```csharp
void ObsSetReplayBufferState(int state, int connection = 0);
void ObsReplayBufferStart(int connection = 0);
void ObsReplayBufferStop(int connection = 0);
void ObsReplayBufferSave(int connection = 0);
```

### OBS Get Scene Item Properties

New sub-action that will make a `GetSceneItemProperties` call to the websocket, and much like OBS Raw, will add the results into your arguments in the form of `props.<path>`

#### New C# Methods for OBS Get Scene Item Properties
```csharp
string ObsGetSceneItemProperties(string scene, string source, int connection = 0);
```

### Run Commercial

Allows you to start a commercial on your channel.  Commercials can be either 30s, 60s, 90s, 120s, 150s, or 180s in duration.

![sub-action-run-commercial-001.png](/sub-action-run-commercial-001.png)

#### New C# Method

```csharp
void TwitchRunCommercial(int duration);
```

### OBS Set Media Source File

Allows you to change the file of an OBS Media source, `%variables%` are supported.

![sub-action-obs-set-media-source-file-001.png](/sub-action-obs-set-media-source-file-001.png)

#### New C# Method
```csharp
void ObsSetMediaSourceFile(string scene, string source, string file, int connection = 0);
```

### OBS Set Image Source File

Allows you to change the file of an OBS Image source, `%variables%` are supported.

![sub-action-obs-set-image-source-file-001.png](/sub-action-obs-set-image-source-file-001.png)

#### New C# Method
```csharp
void ObsSetImageSourceFile(string scene, string source, string file, int connection = 0);
```

### Get Commands

Will give you a list of your commands, into the variable of your choice.  Can be limited down by command group, or if the user doing the command has permissions

![sub-action-get-commands-001.png](/sub-action-get-commands-001.png)

2 variables will be added, the first will be a comma delimited string of your commands, that will be placed in the variable you picked, as well, a list of the commands (for use in C#) will be placed in `[VariableName]List`, so from the screenshot, `%commandsList%` would contain a `List<string>` of your commands

### Get Command State

Using this sub-action you can get the state of a command, whether its enabled or disabled, as well as get the state of a group of commands, if they're all enabled or disabled, or mixed.

#### Variables provided for `Get Command State`

| Variable | Description |
|   ---:|-------------|
| `%commandState%` | The state of the command `true`/`false` |

#### Variable provided for `Get Command Group State`

| Variable | Description |
|   ---:|-------------|
| `%commandGroupState%` | The state of the command group, see table below for information |
| `%commandsEnabled%` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are enabled |
| `%commandsDisabled%` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are disabled |

#### Possible values for `%commandGroupState%`

| Value | Description |
|   ---:|-------------|
| `0` | All disabled |
| `1` | All enabled |
| `2` | Mixed |

### Get Action State

Using this sub-action you can get the state of an action, whether its enabled or disabled, as well as get the state of a group of actions, if they're all enabled or disabled, or mixed.

#### Variables provided for `Get Action State`

| Variable | Description |
|   ---:|-------------|
| `%actionState%` | The state of the action `true`/`false` |

#### Variables provided for `Get Action Group State`

| Variable | Description |
|   ---:|-------------|
| `%actionGroupState%` | The state of the command group, see table below for information |
| `%actionsEnabled%` | A list of action IDs that are enabled |
| `%actionsDisabled%` | A list of action IDs that are disabled |

#### Possible values for `%actionGroupState%`

| Value | Description |
|   ---:|-------------|
| `0` | All disabled |
| `1` | All enabled |
| `2` | Mixed |

### TwitchSpeaker Speak

To simplify uusing TwitchSpeaker with **Streamer.bot**, you can us this sub-action to have messages spoken by TwitchSpeaker.  Before you'd have to use the UDP broadcast sub-action.

#### New C# Method
```csharp
void TtsSpeak(string voiceAlias, string message, bool badWordFilter = false);
```

> This requires you to be using TwitchSpeaker for TTS
{.is-info}

## New C# Methods
### OBS Color Helpers
```csharp
long ObsConvertRgb(int a, int r, int g, int b);
long ObsConvertColorHex(string colorHex);
```

### OBS Helper Methods
```csharp
int ObsGetConnectionByName(string name);
```

### Command Cooldown Methods
> The ID can be retreived by right clicking a command, and clicking the Copy Command ID option
{.is-info}

```csharp
void CommandResetGlobalCooldown(string id);
void CommandAddToGlobalCooldown(string id, int seconds);
void CommandResetUserCooldown(string id, int userId);
void CommandAddToUserCooldown(string id, int userId, int seconds);
void CommandResetAllUserCooldowns(string id);
void CommandAddToAllUserCooldowns(string id, int seconds);
```

# Streamer.bot v0.1.4

* **Fixed:** Various typos
* **Fixed:** Editing a channel reward and setting max per stream works correctly now
* **Fixed:** Creating or duplicating a channel reward correctly says its owned now
* **Fixed:** Add Follow Age Info was not allowing variable entry
* **Fixed:** Streaming with no game category selected would cause a crash
* **Fiexd:** Community Goal contribution event was tied to the wrong underlying event
* **Fixed:** Added a flag to testing the follow event, so it can bypass the built in follow/unfollow protection
* **Fixed:** Potential crash when a websocket or http server port was in use
* **Fixed:** Harden some of the code surrounding Twitch tokens, hopefully less crashes
* **Fixed:** Community goal percent completed calculation was wrong
* **Fixed:** Enabling/disabling commands by group was not correctly working
* **Fixed:** Re-enable maximize box on main window
* **Fixed:** Poll update and complete events were executing the wrong action setting
* **Fixed:** The Twitch Raid start event sends the profile image url at 70x70, updated this to be the larger 300x300
* **Fixed:** PlaySound/PlaySoundFromFolder C# methods were not properly waiting for sound to complete
* **Fixed:** Handle potential crash on startup related to voice control
* **Fixed:** Was not correctly forgetting bot account
* **Fixed:** Poll/Prediction Create, Update and Complete actions were being stored but not shown, the visual bug has been fixed.
* **Fixed:** Find Refs in C# Execute could cause a crash if there is a bad image (a dll) in your application folder
* **Fixed:** Some hardening of code surrounding export to clipboard
* **Fixed:** Fix SetTimerState sub-action not resetting the timer correctly when enabling
* **Fixed:** StreamElements/Streamlabs events no longer try to resolve the user to a seen viewer
* **Fixed:** Fixed community goal help text
* **Fixed:** Fixed a potential deadlock that could occur with OBS Websockets
* **Fixed:** Setting a source's mute state in SLOBS should work correctly now
* **Update:** Credits no longer include the Broadcaster or Bot account in any lists
* **Update:** [Perform Command](#perform-command) sub-action is being updated with new options and capabilities
* **Update:** [ReadLinesFromFile](#readlinesfromfile-and-readrandomlinesfromfile) and [ReadRandomLinesFromFile](#readlinesfromfile-and-readrandomlinesfromfile) were updated to parse variables, and attempt auto-typing
* **Update:** Added `%obsRaw._json%` variable to the OBS Raw sub-action, it contains the result as is, so it could be parsed in a C# action
* **Update:** Missed some variables in [Twitch Prediction](#twitch-predictions) completion event
* **Update:** Missed some variables in [Twitch Polls](#twitch-polls) completeion event
* **Update:** [Commands](#commands) got a bit of an overhaul, check the section for more details
* **Update:** When adding actions, group will be auto filled based on selection
* **Update:** Improved shutdown time
* **Update:** Change how [Twitch Gift Sub Bombs/Gift Subs](#twitch-gift-sub-bombgift-subs) are handled
* **Update:** OBS Set Source Filter State sub-action will now list the global audio sources if they are in use, and will be shown in the list before the scene sources
* **Update:** When switching scenes in most OBS sub-actions, an attempt will be made to pre-select the same named source if possible, this is an ongoing update
* **Update:** Variable replacements now supports inline formatting, using any of the standard C# formatting options, example `%donatedValue:N2%` would give a number with 2 decimal places, if the value is a number
* **Update:** Set Argument subaction can now accept variables as values, be sure to use %s, so you can assign a variable to another variable
* **Update:** Logic If now supports variable names as comparison values, be sure to use %s
* **Update:** UDP Broadcast sub-action now behaves similarly to OBS Raw in how replacements are done, invalid characters should no longer be an issue, and numbers will be treated as numbers
* **Update:** Add new `%messageCheermotesStripped%` variable to a cheer event, that retains all the emotes, and only stiprs cheermotes
* **Update:** Allow variable usage for SLOBS Set Active Scene sub-action
* **Update:** Made the text entry for the Twitch Send Message sub-action a bit biger and wrap lines, so more can be seen
* **New:** New [Hot Key Support](#hot-key-support)
* **New:** [Confirimation dialog](#confirmation-dialogs) when deleting an action, a sub-action, or all sub-actions
* **New:** [Confirimation dialog] when closing bot.
* **New:** Minimize/Close to tray option
* **New:** Expanded OBS capability with [OBS Events](#obs-events) being able to trigger actions
* **New:** New [OBS Take Screenshot](#obs-take-screenshot) sub-action
* **New:** New [OBS Set Audio Track State](#obs-set-audio-track-state) sub-action
* **New:** New [OBS Set Media State](#obs-set-media-state) sub-action
* **New:** New [Twitch Set Channel Title](#twitch-set-channel-title) sub-action
* **New:** New [Twitch Set Game](#twitch-set-game) sub-action
* **New:** Add ability to enable/disable all actions in a group from context menu
* **New:** Block port 4444 from being used for **Streamer.bot's** own internal websocket server
* **New:** Introduced a new option for commands, [Command Cooldown Action](#command-cooldown-action), check for more details
* **New:** You can now drag sub-actions around to move them **this is still a bit experimental and might have some issues**
* **New:** Ogg Vorbis is now a supported playback format for sound files
* **New:** Commands now have a **Case Sensitive** option
* **New:** Added C# methods for creating [Twitch Predictions](#twitch-predictions)
* **New:** Add C# methods to enable/disable [Commands](#commands)
* **New:** Added 2 new variables, `%createdAt%` and `%accountAge%` to the Get Target Info sub-action, accountAge will be given in seconds
* **New:** Update [Twitch Polls](#twitch-polls) to be able to handle the `/endpoll` command (Poll Terminated action)
* **New:** Add option to export actions to file
* **New:** Add indicator to exporting to clipboard that it was successful
* **New:** Add new context menu item when right clicking a user to perform some twitch actions, at the moment, just banning and adding/removing mod/vip status
* **New:** New Set Command Group State sub-action
* **New:** New Set Action Group State sub-action
* **New:** Quote settings now shows all your quotes, and can be deleted, this is just the start of UI for quotes
* **New:** Add ability to duplicate a group and all of it's sub-actions
* **New:** When connecting to Twitch, your list of mods and vips are updated automatically
* **New:** [Experimental Linux Support](#experimental-linux-support) **READ THIS SECTION FOR IMPORTANT INFORMATION**
* **New:** Add new sub-action for enabling/disabling slow mode in your twitch channel
* **New:** Add new sub-action for creating a clip, as well as a C# method. **NOTE, There is no control over the clip created, title, length, etc**
* **New:** Add new sub-action for creating a stream marker, as well as a C# method; you can provide a description for the marker
* **Misc:** Update some libraries that are used

## Hot Key Support
After much requesting, it's here, Global Hot Key support!  There is also a new sub-action to send keyboard presses! 

The keys you can use for creating a global hotkey are currently limited to keys that make sense, and can always be expanded.

The sub-action for keyboard presses, at the moment, is really meant for pressing global hot keys, and may evolve over time to be able to specify a specific window/application.

![sub-action-keyboard-press.png](/sub-action-keyboard-press.png)

## Perform Command
The **Perform Command** sub-action has had a bit of an overhaul to give you more options in setting up to run a command.

![sub-action-perform-command.01.png](/sub-action-perform-command.01.png)

The new additions allow you to set the working directory, the arguments to use (which supports variable replacement), as well as being able to set environment variables (also supporting variable replacement).

**Note:** *There was a bug in the old version where it could not run commands with arguments properly.*

For example, the following could be used for executing a python script.

| Property | Value |
|      ---:|-------|
| Command | `C:\Python27\pythonw.exe` |
| Working Directory | `C:\StreamStuff` |
| Arguments | `C:\StreamStuff\sub-printer.py` |

Environment Variables could be:

| Key | Value |
| ---:|-------|
| `USER` | `%user%` |
| `TIER` | `%tier%` |
| `MESSAGE` | `%message%` |

## ReadLinesFromFile and ReadRandomLinesFromFile
Read Line From sub-actions have options to now parse variables in the line read, and to auto-type instead of always adding as a string

![sub-action-readlinesfromfile-01.png](/sub-action-readlinesfromfile-01.png)

![sub-action-readrandomlinefromfile-01.png](/sub-action-readrandomlinefromfile-01.png)

## OBS Events
New with this version, you can now assign triggers to events that OBS transmits across the websocket connection.

![obs-events-01.png](/obs-events-01.png)

The data that an event emits, is added onto the arguents the same way it is with results from `OBS Raw`, as well as a `%obsEvent._json%` variable that can be parsed in C# (`JObject.Parse()`) for easier use.

OBS events are per-connection based.

## Confirmation Dialogs
When closing **Streamer.bot** you'll be prompted if you're sure you want to close, with the option of not asking again.

![close-prompt.png](/close-prompt.png)

When you delete an action, or a sub-action, you will be prompted to confirm the deletion, with the option of not asking again.

![delete-confirm.png](/delete-confirm.png)

You can reset these confirmations under the `User Interface` tab in `Settings`

## Twitch Predictions
Seems I missed adding in some variables to the completion event, unlike polls where a winner is determined by a fixed vote, predictions are resolved, and the broadcaster or a moderator pick the specific winner.

In addition, I added a `%prediction._json%` argument, which contains a JSON string of the event that can be parsed in C# (`JObject.Parse()`) for easier use.

| Value | Description |
|   ---:|-------------|
| `%prediction.winningIndex%` | Either a 0 or 1 depending on which outcome was chosen as the winner |
| `%prediction.winningOutcome.id%` | The ID of the winning outcome |
| `%prediction.winningOutcome.title%` | The title of the winning outcome |
| `%prediction.winningOutcome.users%` | How many users voted for this prediction |
| `%prediction.winningOutcome.points%` | The total number of channel points used by users |
| `%prediction.winningOutcome.color%` | The colour of the winning outcome |

### Prediction C# Methods
There are 4 new C# methods that can be used to create a prediction from C# code.

```csharp
string TwitchPredictionCreate(string title, string firstOption, string secondOption, int duration);
void TwitchPredictionCancel(string predictionId);
void TwitchPredictionLock(string predictionId);
void TwitchPredictionResolve(string predictionId, string winningId);
```

## Twitch Polls
Even tho a poll can technically end in a tie, I added the winning choice information into the arguments.

In addition, I added a `%poll._json%` argument, which contains a JSON string of the event that can be parsed in C# (`JObject.Parse()`) for easier use.

| Value | Description |
|   ---:|-------------|
| `%poll.winningIndex%` | The index of the winning choice, from 0 to 4 |
| `%poll.winningChoice.id%` | The ID of the winning choice |
| `%poll.winningChoice.title%` | The title of the winning choice |
| `%poll.winningChoice.votes%` | Number of regular votes |
| `%poll.winningChoice.bitVotes%` | Number of bit based votes |
| `%poll.winningChoice.rewardVotes%` | Number of channel point based votes |
| `%poll.winningChoice.totalVotes%` | Total number of votes for the choice |

### New Action
When using `/endpoll` in your chat to stop an active poll, its sent through as terminated, not completed; a new assignable action to the terminated event has been added.

## Commands
After seeing and hearing the feedback, commands got a bit of an overhaul.

To start with, something simple, when you add a new command, if you happened to right click on an existing command and picked add, the new command will be auto-set to the group of the selected command.  Right clicking add while on a group line itself, will also auto assign the group when adding a command.

You can now have multiple "commands" for a single command, also, Regex based input is supported.

> Regex comparisons can be heavy; even with the precompilations that exist for C#, they can become slow if the expression itself is not optimized.  There are no limits on how many you can create, but just be aware, every message that comes through is checked against all commands to see if any should be run.
{.is-warning}

The introduction of regex, is just simple at the moment, and may get a bit more complex afterwards (for example, regex capture groups being added as arguments)

One other thing to note, the `%rawInput%` variable for commands, specificially the **Start** location, auto strips the command from the start, at the moment, with a regex based command, it will behave like **Anywhere** and not remove the matched section(s), I may alter this slightly and add a 2nd variable that gives you both, one with, and one without, I'm unsure yet.

![commands-multi-01.png](/commands-multi-01.png)

![commands-regex-01.png](/commands-regex-01.png)

### Command C# Methods
Two new C# methods were added to be able to enable/disable a command.  Unlike other methods that only need a title, this requires the ID of the command, this can be retreived by right clicking on a command and selecting `Copy Command Id`

```csharp
void EnableCommand(string id);
void DisableCommand(string id);
```

## Command Cooldown Action
From the suggestion board, letting a user know that a command was on cooldown was requested, and instead of just hard coding this, I've added this as a configurable action instead.

A cooldown action can only trigger from a command that has a location of `Start` or `Exact`, regex based commands, or anywhere location will not trigger this action, even if it is on cooldown.

Also, only a `Message`, `Subscription` and `ReSubscription` can trigger a cooldown action.

There is a new column in the `Commands` list that shows the `Cooldown Action` associated with a command.

Available variables:

| Value | Description |
|   ---:|-------------|
| `%command%` | The command that was used |
| `%cooldownLeft%` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left |
| `%globalCooldownLeft%` | How many seconds are left for the global cooldown of the command |
| `%userCooldownLeft%` | How many seconds are left for the user cooldown of the command |

There is also a new websocket event that can be subscribed to, `CooldownEvent` for `Commands`

![sub-action-commandcooldown-01.png](/sub-action-commandcooldown-01.png)

The most basic subaction you could add, would be a `Twitch Message` with the message `%user%, %command% is on cooldown for %cooldownLeft%s`

## Twitch Gift Sub Bomb/Gift Subs
In previous versions, when someone dropped a gift bomb (more then 2 gift subs in a single go), only the gift bomb event itself was triggered, and all associated gift sub events for it were silently discarded.

With this version, the gift subs are no longer discarded, they are now also sent, and there is an argument `%fromGiftBomb%` that will exist. If this is true, the sub is from a gift bomb, if false, its not.

I've also added `%subBombCount%` which will give the number of gift subs, if ths gift sub belongs to a gift bomb.

One last new argument is `%cumulativeMonths%`, this can have how many months the user receiving the gift sub has been subscribed for, if its 1, they are a new subscription, if its > 1, then its a resub.  There are chances where it can be 0 from what I've seen.  So this value could be used to welcome a new gifted subscriber.

## New Sub-Actions

### OBS Take Screenshot
Up until now, you had to use OBS Raw to take a screenshot in OBS, here is a sub-action ot make things a bit simpler.

![sub-action-obs-takescreenshot-01.png](/sub-action-obs-takescreenshot-01.png)

`Scene`, `Source` and `File Path` all support variable replacements, and after a screenshot is successfully taken, the full file path is added back onto the arguments as `%screenshotFile%`.

There is a new date time friendly variable that can be used, `%filedatetime%` which is of the format `yyyyMMdd.hhmmss`.

### OBS Set Audio Track State
With this sub-action you can alter which audio tracks a source can be active on

![sub-action-setaudiotrackstate-01.png](/sub-action-setaudiotrackstate-01.png)

> This sub-action ***requires*** obs-websocket version 4.9.1
{.is-info}

## OBS Set Media State
Control the state of media playback, you'll be able to `Play`, `Pause`, `Restart`, `Stop`, `Next`, `Previous` the specified media.

![sub-action-obs-setmediastate-01.png](/sub-action-obs-setmediastate-01.png)

The following C# methods were also added to control media via code.
```csharp
void ObsSetMediaState(string scene, string source, int state, int connection = 0);
void ObsMediaPlay(string scene, string source, int connection = 0);
void ObsMediaPause(string scene, string source, int connection = 0);
void ObsMediaRestart(string scene, string source, int connection = 0);
void ObsMediaStop(string scene, string source, int connection = 0);
void ObsMediaNext(string scene, string source, int connection = 0);
void ObsMediaPrevious(string scene, string source, int connection = 0);
```

## Twitch Set Channel Title
Using this sub-action, you'll be able to set the title of your channel, either to a fixed value, or using variables.

![sub-action-setchanneltitle-01.png](/sub-action-setchanneltitle-01.png)

The following C# method was also added to set your channel title via code.
```csharp
bool SetChannelTitle(string title);
```

An example action that you can assign to a `!title` command
```
TlM0RR+LCAAAAAAABACVVNmOm0gUfR9p/sGylLdgUSx2EykP3XTbhlYzwhuYoR9qA9MulrDYjaP8+xQQp7GtaBQsC7jn1rnnnuLW97//GgyGB5oXUZoMvwzA5zaQwJjyt+GSlvoOJgllq6hkdNihEJc8u+AJ/zbvg8H37sahiDTLFBWiAMhjQUUTRVDGgAp36hgKqiJTWVEIgEDuuNpF3ypaNeWSirGPKE0gYrThK/OKfsR72gY/xQ166tqcME+rrEny+NWLQ3aEdbGomlYDyIoebQ4Tksb3bWu3KE4TXOU5Tcpb7MaOC0valLLVx/V8yuHRSLKq/PShqmecLGp3QFMlYUwJERQZEgGKARYoVUQJUDIZg/HVwiONwl2jShyJl0hZZ01NoF6Gz95cuN1pSAh9b5g+oj8+/66l3jasDN7dghYVK6/EEVrgPMp+ejq8QveUZvcsOtAbT7sdoQHljmN6ZW0L6l983+GC02Ph+y8RztMiDcqR9bTy/WnOtR3TfO/7B2UkjmRRBprvxwVOcxahEWFs2Kd7vayL6pLqKWm7I66VoRiHa5mdyGxT/nMUnx/t7Egcs4DOS7iV3ndYfglt8GAsHZXHVMbxyaOdmni+idCMvRkz84CkY7hwd2wrb0RvGWYNTjmXbjNp6xohljdvW2lzwvW9ZjxZB5R4DCd2tZlpOpK0wnOm1fNsWnuyhYxkkZHZO1v/WmOS51Vh6eHeJPG0Nubmjois4vVF41EMt66ZYFBEOJ7KXOORuHbkLtU1ApaIY1Z5dZh1faWm7rDY0Hcn4lhvnmudnu1WY9sPvz+un8JqLW0q7wkwLFs7T1pzwFxDd1F4y4eT59ohmd2NjXlZb11iouQBkLkYnfUFHR9Dc4u1nG4X19eWvdTVleeo+5XDe5KmCfdpb7BNteVec24R1Wd+JqLZ+v9q1J67ADhWQjI3gddiTON7w//p16svMcspTuMsYr/5FAllsF6WML8d/970KjggGgKqcKdNVEGZUFFAeAIETCkKAsB/WPrT6dWa608HGPQG+Pz4en1gzRqadrRe++ccYzArKOmhHdgSdZndgX0Gf/wHhK9EBUQGAAA=
```

## Twitch Set Game
Using this sub-action, you'll be able to set the game for your channel, again using a fixed game that you can set from a list, or by using variables

![sub-action-setchannelgame-01.png](/sub-action-setchannelgame-01.png)

![sub-action-setchannelgame-02.png](/sub-action-setchannelgame-02.png)

The following C# methods were also added to set a game via code.
```csharp
GameInfo SetChannelGame(string game);
bool SetChannelGameById(string gameId);

public class GameInfo
{
		public int Id { get; set; }
		public string Name { get; set; }
		public string BoxArtUrl { get; set; }
}
```

An example aciton that you can assign to a `!game` command
```
TlM0RR+LCAAAAAAABACVVctu2kAU3VfqPyCk7mLkJ+DughPATuMUiG1wncW8MA7jR/2Amqr/3hkbBAF1UUsI5p65Z84913f4/flTp9PdkbyI0qT7tSPdNYEExIStugtSGhuQJIROeKQFASrZ5oLhP/i60/ndfjEowjwLA62P4AALfayqgirJQwGA/oAt+0ofaiKBUr/lapJ+VqTipyUVpecoSQCkhPOVeUXO8QtpnaO2zllcsyXM0yrje3z2XMQB3YO6mFe80DWgxQVrDhKcxvdNZbcoShNU5TlJylvsxo0PjjRbirTKERct3n2Ih8dSvuRgbyZZVX7p3m4wG0uvgNZnoKqqBpW1oANREVQVi4KuKKIwJAoZAl0fDofSVeKeROGGVyH2rsSUdcbFSP0rCUcvPzSn1ZBg8osznaN/7v5lwUXXeLPmpKhoeaUNkwLlUXZswXXJW0KyexrtyE0L2gaSNWENQuSqEw1ofA0Cj+lN90UQPEcoT4t0Xfbsx9cgGOdMzz7Nt0GwU3tiTxEVSQ+CuEBpTiPYw5R2L+nePp4L65IYKW6Kw0s7gzEKHYUe8MQtX/bi08Ms22PPKoD3HK7kXxukPIczaWQuPI3FNMrwwcMstdDUjeCEvpsTawflfThfbuhKcUV/EWYcJ4zLmFF5tTRDpLjvK9k9oPpeNx/tHUx8ipJZ5U50A8p64Xvj6mkyrn3FhmaMN9BzX7Fnv/tL+2BSMWt1pZbh0dg0NocT9jRrzmj0nM7y5XHpOxrjcMLvi9EGxfjg1Vay8iT6GjNsYeFvdL5zlHnN6kmejO0p/8F5DCtHdiv/UaJIsTe+7DDAmvJcc2pTbIxEeEhDIjcaX3h8vTAbfSxfbzW6BZId2wi3Rw+2Fo7HtTm1NlikFfNNNB/EcLW0EiQVEYrHCvN2j5ezaLnQHCjZIopp5dfhkXdrcf+/UZvCeG7zulcepgyIXE/LYawrMBo19b1Eo8GZb66b0bG2pdjoQbEr4qVVmdN5jT2nwdbMQ/65enuznKA0ziL6j9cXEwrqRQny2xvmYuA1fYg0HSCBQCIKKh6obODVgbCWIegrcA36ZPC/A6/z539nXrqY+dPPt+s7ccJpmnF8u7xKKQVZQfAF2oINUbuz/Us4gX/+AqlLhx2lBgAA
```

## Experimental Linux Support

> There is no guarentee this will work 100%, there are areas of the app that may not function correctly, so this will be a complete work in progress depending on time/effort.
{.is-warning}

It is possible to run this current version (**0.1.4**) using wine/wine64 within Linux

The entire network stack was re-written to make this possible, as it was a major blocker.

I've been doing some tests using the staging version of Wine, which is v6.19 in Ubuntu 20.04 LTS.

For your Wine setup, you'll want the following:
```
winetricks dotnet472
winetricks d3dcompiler_47
winetricks dxvk
```
You will also want to make sure gnutls (for 32-bit, lib32-gnutls).

This information should also apply to TwitchSpeaker, one area that will not work in TwitchSpeaker are SAPI5 voices, and the Azure voices may also not work. Again, this is very experimental.

A dedicated page on the wiki will likely be created for those who are using/testing it under Linux to list what works and what the current issues are.

> Running **Streamer.bot** and/or **TwitchSpeaker** under Linux is considered to be experimental, so expect bugs/issues.
{.is-warning}

# Streamer.bot v0.1.3

* **Fixed:** Logic if sub-action for does exist, code path was unreachable
* **Fixed:** Importing actions which contained obs actions, was not correctly defaulting to first configured obs instance
* **Fixed:** Importing actions which contained ClearActionQueue and SetActionQueuePauseState
* **Fixed:** ClearActionQueue and SetActionQueuePauseState to handle if an invalid queue has been selected
* **Fixed:** Pyramids, a change to the way emotes were handled broke this feature
* **Fixed:** Stream Update could cause a crash if your category was empty, On Connect was enabled, and at least 1 Game action was configured 
* **Fixed:** Typo in the Gift Bomb event, was `totalGits`, should have been `totalGifts`
* **Fixed:** Assigning an action to a group using the context menu no longer causes all groups to expand
* **Fixed:** Hosting event had the potential to cause a crash
* **Fixed:** Clicking cancel when creating a poll will no longer warn that poll could not be created
* **Fixed:** OBS Raw variable replacement tries to be type aware, if the variable is a number, it won't put it in quotes for instance
* **Fixed:** Possible crash when removing/updating a speech to text command when its not actively running
* **Fixed:** Play Sound From Subfolder sub-action was setting the folder properly when editing
* **Fixed:** Get Random Number sub-action was not linked to the correct edit action (whoops?)
* **Fixed:** Quote messages were not being sent over bot account if it was connected, this will probably change to actions in another release for better control
* **Fixed:** If the logic if sub-action was not set to run immediately, it would not break if the after action was set to this
* **New:** The Rewards -> Configure Rewards sub-action has been updated a bit, window is now resizeable and added a context menu for moving rewards as well
* **New:** Mask the Streamlabs and StreamElements tokens, with a show/hide button
* **New:** Added [Subscriber](#subscriber-only) and [Emote](#emote-only) Only Sub-Actions
* **New:** Added Subscriber and Emote Only methods for Execute C# Code
* **New:** Added new Sub-Action [Read Lines From File](#read-lines-from-file)
* **New:** Channel rewards are now groupable, and sortable by `Name`, `Cost` and `Owned` within there groups
* **New:** Added ability to enable/disable/pause/unpause all owned rewards in a group through context menu
* **New:** Added ability to enable/disable all commands in a group through context menu
* **New:** Added [Fetch Url](#fetch-url) sub-action
* **New:** Added [Pick Color](#pick-color) sub-action
* **New:** Copy pasta sub-actions!  Be sure to [read below](#copy-pasta-sub-actions) for specifics
* **New:** Added a [Comment](#comment) sub-action
* **Updated:** As per a few suggestions, the **Speech To Text** tab has been renamed to **Voice Control**
* **Updated:** First pass over the **[Groups](#groups)** section has started
* **Updated:** Execute C# Code [Find Refs](#find-refs) has been updated a bit, and is a lil more forgiving when it tries to add the needed references
* Misc fixes/tweaks that I probably forgot to write down

## Copy Pasta Sub-Actions
As more of a QoL improvement, I have started implementing some basic copy and paste functionality.  First up to get this capability is the sub-actions.

While it does copy data to your clipboard, meaning it could be shared; it is **not** recommended to, currently, when you paste an action, no real sanitization and checks are done (*yet*), as it is meant to be pasted back into your own running instance of **Streamer.bot** which has all the supported components setup already (i.e., OBS connection, Queues, etc).

Also, at the moment, you can only copy 1 sub-action, this may change in the future when I start enabling multi-select capabilities, but, it's 1 step at a time.

## New Sub-Actions

### Subscriber Only
This will let you enable or disable Subscriber Only mode for your channel

### Emote Only
This will let you enable or disable Emote Only mode for your channel

### Read Lines From File
With this sub-action, you'll be able to read all the lines of a file into variables.  It will put each line of the file into `%line#%` where # is the line number starting from 0. `%lineCount%` will also be added with the total number of lines.

### Fetch Url
You can now fetch simple api endpoints and put them into a variable of your choosing. The Url supports variable parsing.

![sub-action-fetch-url-01.png](/sub-action-fetch-url-01.png)

### Pick Color
Added a way to pick a colour and put it on the arguments for an action.

![sub-action-pick-color-01.png](/sub-action-pick-color-01.png)

When this sub-action is run, the follow variables are added to the arguments

| Variables | Description |
|       ---:|-------------|
| `%var.color.a%` | The alpha value |
| `%var.color.r%` | The red value |
| `%var.color.g%` | The gren value |
| `%var.color.b%` | The blue value |
| `%var.html%` | The html color code |
| `%var.htmlalpha%` | The html color code with alpha value |
| `%var.obs%` | The color as an OBS ABGR value |

> This may evolve a bit in the future, either by way of more capabilities, or moving it to a different area
{.is-info}

### Comment
Just an action that you can put text into, that'll show up as a comment, pre and post fixed with **, it will not be executed when the action is run.

## New C# Methods
2 new methods are available for enabling/disabling Subscriber/Emote only modes
```csharp
void TwitchSubscriberOnly(bool enabled = true);
void TwitchEmoteOnly(bool enabled = true);
```

## Groups
The groups section has had a few updates.  The list of groups has been udpated with some context menu options.  You can toggle the Bot status of a group, delete, clear a group; as well as export a group to a file, and import from a file.

There is more work to be done here. These are the first steps.

## Find Refs
Using the Jokes code that is in the examples channel of the discord, I went through and tried to get **Streamer.bot** to be a bit more lenient on how it adds/removes references when you click the Find Refs button on the Execute C# Code dialog.  It is still not perfect, nor will it ever be, as trying to "figure" out what references are required is not an easy thing to do without it taking a while.

# Streamer.bot v0.1.2

Visit [Streamer.bot 0.0.61](#streamerbot-v0061), [Streamer.bot 0.0.62](#streamerbot-v0062), [Streamer.bot 0.0.63](#streamerbot-v0063), [Streamer.bot 0.1.0](#streamerbot-v010) and [Streamer.bot 0.1.1](#streamerbot-v011) to see all the shiny new features and updates.

* **Critical fix** for actions not working correctly

# Streamer.bot v0.1.1

Visit [Streamer.bot 0.0.61](#streamerbot-v0061), [Streamer.bot 0.0.62](#streamerbot-v0062), [Streamer.bot 0.0.63](#streamerbot-v0063) and [Streamer.bot 0.1.0](#streamerbot-v010) to see all the shiny new features and updates.

### Some fixes/changes

* **Fixed:** Some typos
* **Fixed:** SetSceneFilterState sub-action not populating filter list
* **Fixed:** not being able to add SLOBS Get Current scene sub-action
* **Fixed:** Crash when adding a Speech To Text command when it is not listening
* **Fixed:** Potential crash when retrieving paginated data from Twitch API
* **Fixed:** Streamlabs typo, was firing the wrong event for the generic donation action
* **Fixed:** Set queue pause state not having a default state when adding the sub-action
* **Fixed:** Importing actions causing all groups to become expanded, and slow updating of adding the actions
* **Fixed:** Pausing a queue, if it had actions queued, they still ran, seems I missed a scenario
* **Fixed:** An issue with WebsocketSend in C# not actually sending data
* Add new options for Websocket Client settings to specify TLS options
* Update OBS Raw
* Some UI QOL improvements, both the main and settings tabs are re-orderable, and can hide unused tabs
* Save button gives an indication something is happening
* Some fixes surrounding OBS Websocket and authentication states (still some quirks)
* Add a Name property to OBS Raw to help differentiate them
* Remember collapsed sub-action groups
* Add column to Channel Reward to indicated if we own the reward
* Update OBS and SLOBS set GDI text to support multi-line text entry
* Add Collapse/Expand all to context menu for actions
* Enable and fix Twitch Host event
* No longer allow empty named actions ;)
* Add enabled toggle to action dialog, for enabling/disabling actions
* Creating a new timer did not have the repeat option checked, as it says in the description
* Founder badge was not being associated to a user as being subscribed
* Add `%isSubscribed%`, `%isModerator%`, `%isVip%` to action arguments
* Add a new sub-action `Clear Action Queue` to clear a blocking queue
* Move separators in sub-action context menu, grouping the menu items a bit better
* Add `Ctrl + Home` and `Ctrl + End` shortcut keys for moving sub-actions to top/bottom
* Misc fixes/cleanup

Join the [Discord](https://discord.gg/zuXpPpgD5K) if you have any questions, would like to share what you've created, or or would like to lend a hand!

### OBS Raw
I have gone through and updated how OBS Raw behaves, previously it would only return if the status of the call was a success or not.  Now, it will take all the JSON values returned and add them onto the argument list in the form of `obsRaw.{path}`, so `status` is now in `obsRaw.status`, so you can check this if the call was successful or not.  The values that are put on the arguments are dynamic and depend on what you are sending.

A note, array will be added as `obsRaw.data.value[0].id` for example.

If you are using OBS Raw through C#, you will be given back the JSON as a string, so you can use a JObject.Parse() to convert it to something usable in your code.

#### Variable Replacement

You can also use variables in OBS Raw.  To use variables, just add the variable inbetween quotes for your json property

Example:
```json
{
  "test": "%variable%"
}
```

The underlying code will go through all the properties and do any variable replacements it finds.

### Twitch Hosts
Seems as tho this event was "broken", so, went through, fixed it up, and re-enabled it.  One note, viewer count according to Twitch's own references should be available, but what it says should happen doesn't.

The event does provide a `%viewers%` variable, which is best guess accurate, utilizing an API call to retrieve information.




# Streamer.bot v0.1.0
Welcome to Streamer.bot v0.1.0 public release!

This has been over a year in the making, and its now available for anyone to use!

I hope it helps elevate your stream 😄 

Just as a quick note, I expect there to be bugs, please do report them so I can get them fixed!

Visit [Streamer.bot 0.0.61](#streamerbot-v0061), [Streamer.bot 0.0.62](#streamerbot-v0062) and [Streamer.bot 0.0.63](#streamerbot-v0063) to see all the shiny new features and updates.

### Some fixes/changes

* Fix SetActiveScene not parsing variables

Join the [Discord](https://discord.gg/zuXpPpgD5K) if you have any questions, would like to share what you've created, or or would like to lend a hand!



# Streamer.bot v0.0.63
Visit [Streamer.bot 0.0.61](#streamerbot-v0061) and [Streamer.bot 0.0.62](#streamerbot-v0062) to see all the shiny new features and updates.

### Some fixes/changes

* Log files have been moved to their own logs folder
* All settings and cache files are now in their own data folder
* Change what modules are merged
* Tweak finding references for Execute C# code
* Fix delete key not removing references properly in Execute C# Code sub-action
* Fix OBS/SLOBS visibility state not setting a default state, which could lead to a crash
* Commands became unusable after editing a command, woops
* Added 2 new scopes, to create clips, and to manage your broadcast (update title, set game, etc)  The app will notify you that you'll need to re-auth
* Added new Action Added/Updated/Deleted events, mostly to better support StreamDeck plugin
* Misc fixes/etc that I've probably forgot
* Add top/bottom move otpions for moving sub-actions
* Fix creating rewards not having action assigned if one was chosen
* New app icon

### StreamDeck
Was tinkering around with StreamDeck plugins and managed to get a basic one working, you can create a new button and give it an action.  My experience with writing these plugins is very limited, so this version may not advance very far, but hopefully a more advanced one may eventually takes its place.

[StreamDeck Streamer.bot](https://github.com/nate1280/streamdeck-Streamer.bot)

### Logs and Settings
When starting Streamer.bot without a logs or data folder, it will auto-create these folders, and move any existing logs and settings into this folder for you, and carry on like normal.

### EXE Changes
You'll notice that the archive is a bit large, and contains more files now.  I've decided to split all System/Microsoft libraries out of the merge and will now be alongside the application.  I'm hoping that this might reduce the number of false positives in anti-malware applications.

### Execute C# Code
Finding refs for Execute C# has been improved, and seems to do a better job at finding system related references, this is still an ongoing tweaking.

This also occurs during an import when a C# sub-action is found, it will re-find references for your local system and update them, there still may need to be manual finding of refs, and the import/export process will likely improve for these scenarios (i.e. including external libraries, and more)









# Streamer.bot v0.0.62
Visit [Streamer.bot 0.0.61](#streamerbot-v0061) to see all the shiny new features and updates.

Just a small fix

* Fix double clicking on commands
* Possible startup error fix
* Fix strange behaviour with new control used for grouping in actions/commands

> **NOTE**
> Windows Defender may give a false positive, I believe this is due to the inclusion of the Roslyn compilers which power the C# compiling capabilities. The fact they're there and there is code within the app to compile stuff itself I believe is what's causing the flagging, I'm not sure how to remedy this.
{.is-warning}





# Streamer.bot v0.0.61
* Fix running action from C#, possible caught crash and the action would not run
* Add new options to Execute C# Code to support delayed start
* Updated Execute C# Method sub-action to run on UI thread
* Fix crash when editing play sound from folder, when folder no longer exists
* Fix editing channel rewards, global cooldown limit was too low causing a crash
* Update actions list with groups, actions are sorted and groups can be collapsed
* Update commands to allow groups to be collapsible.
* Collapsed groups in actions and commands will be remembered and set on launch
* Add new menu item when right clicking on sub-action to provide capabilities to run certain methods tied to the sub-action
* First pass of updating groups for future changes, this converts and alters underlying data
* Update cheers not being included in credits
* Fix custom server sockets, sending data was not working correctly
* Add a few new menu options to copy the IDs of Actions and Commands
* Add ability to enable/disable actions, along with a new sub-action to set an actions state and C# methods
* Fix FileWatcher, had a few typos with menu interactions
* More fixes/updates I probably forgot

### New Features

#### Sub-Actions
As an experiment, I am adding new custom menu item to run certain methods contained within a sub-action.  At this moment, this only applies to Execute C# Code, there are 2 new menu items to Compile, and Unload; which will trigger a compile and init of the code, or it will fully unload/dispose of the code (like what happens in a shutdown)

#### Execute C# Code
There is a new option for a delayed start, as well as an option to run a method on a UI thread.  The reason for this addition is, you're able to us WinForms and create fully backed UI code.  But to do this, anything WinForm related **MUST** originate from a UI thread.  This usage is fairly advanced, so if you're in a position to do this, then you'll understand more.

I have added 3 methods to be able to create and end Twitch Polls

```csharp
bool TwitchPollCreate(string title, List<string> choices, int duration, int bitsPerVote = 0, int channelPointsPerVote = 0);
void TwitchPollTerminate(string pollId);
void TwitchPollArchive(string pollId);
```

Added 2 new methods that will allow you to enable/disable actions

```csharp
void DisableAction(string actionName);
void EnableAction(string actionName);
```




# Streamer.bot v0.0.60
* Fix arguments for message/cheer, relating to emotes
* Fix Streamlabs/Streamelements ranges for donation amounts, seems I forgot to wire that up
* Fix handling increment in GlobalSet, wasn't working with new variables correctly
* Misc fixes/tweaks




# Archives
[Streamer.bot 0.0.59](/en/Changelogs/Archives/Version-0059)
[Streamer.bot 0.0.58](/en/Changelogs/Archives/Version-0058)
[Streamer.bot 0.0.57](/en/Changelogs/Archives/Version-0057)
[Streamer.bot 0.0.56](/en/Changelogs/Archives/Version-0056)
[Streamer.bot 0.0.55](/en/Changelogs/Archives/Version-0055)
[Streamer.bot 0.0.54](/en/Changelogs/Archives/Version-0054)
[Streamer.bot 0.0.53](/en/Changelogs/Archives/Version-0053)
[Streamer.bot 0.0.52](/en/Changelogs/Archives/Version-0052)
[Streamer.bot 0.0.51](/en/Changelogs/Archives/Version-0051)
[Streamer.bot 0.0.50](/en/Changelogs/Archives/Version-0050)
[Streamer.bot 0.0.49](/en/Changelogs/Archives/Version-0049)
[Streamer.bot 0.0.48](/en/Changelogs/Archives/Version-0048)
[Streamer.bot 0.0.47](/en/Changelogs/Archives/Version-0047)
[Streamer.bot 0.0.46](/en/Changelogs/Archives/Version-0046)
[Streamer.bot 0.0.45](/en/Changelogs/Archives/Version-0045)
[Streamer.bot 0.0.44](/en/Changelogs/Archives/Version-0044)
[Streamer.bot 0.0.43](/en/Changelogs/Archives/Version-0043)
[Streamer.bot 0.0.42](/en/Changelogs/Archives/Version-0042)
[Streamer.bot 0.0.41](/en/Changelogs/Archives/Version-0041)
[Streamer.bot 0.0.40](/en/Changelogs/Archives/Version-0040)
[Streamer.bot 0.0.39](/en/Changelogs/Archives/Version-0039)
[Streamer.bot 0.0.38](/en/Changelogs/Archives/Version-0038)
[Streamer.bot 0.0.37](/en/Changelogs/Archives/Version-0037)
[Streamer.bot 0.0.36](/en/Changelogs/Archives/Version-0036)
[Streamer.bot 0.0.35](/en/Changelogs/Archives/Version-0035)
[Streamer.bot 0.0.34](/en/Changelogs/Archives/Version-0034)
[Streamer.bot 0.0.33](/en/Changelogs/Archives/Version-0033)
[Streamer.bot 0.0.32](/en/Changelogs/Archives/Version-0032)
[Streamer.bot 0.0.31](/en/Changelogs/Archives/Version-0031)
[Streamer.bot 0.0.30](/en/Changelogs/Archives/Version-0030)
