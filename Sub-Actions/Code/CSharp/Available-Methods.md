---
title: C# Available Methods (Coming Soon)
description: Reference of all methods that can be accessed via the CPH object available in Streamer.bot
published: false
date: 2022-10-29T20:52:31.783Z
tags: 
editor: markdown
dateCreated: 2022-10-28T16:37:34.887Z
---

Below are all the methods that can be accessed via the `CPH` object that is is available in your inline scripts

> The object name, `CPH`, is a holdover from earlier versions of the Streamer.bot, when it was known as *Channel Points Handler*.
> To prevent any breakage, and as a bit of nostalgia, `CPH` was left alone when we renamed to Streamer.bot
{.is-info}

If there are methods missing, make the suggestion to get them added in!

## General
* [<i class="mdi mdi-iframe primary--text"></i> **Application**](/Sub-Actions/Code/CSharp/Available-Methods/Application)
* [<i class="mdi mdi-server-network primary--text"></i> **Servers and Clients**](/Sub-Actions/Code/CSharp/Available-Methods/Servers-and-Clients)
* [<i class="mdi mdi-lightning-bolt primary--text"></i> **Actions**](/Sub-Actions/Code/CSharp/Available-Methods/Actions)
{.btn-grid .my-5}

## Platforms
* [<i class="mdi mdi-twitch text--twitch"></i> **Twitch**](/Sub-Actions/Code/CSharp/Available-Methods/Twitch)
* [<i class="mdi mdi-youtube text--youtube"></i> **YouTube**](/Sub-Actions/Code/CSharp/Available-Methods/YouTube)
{.btn-grid .my-5}

## Broadcasters
* [<img src="https://streamer.bot/img/integrations/obs.svg"> **OBS**](/Sub-Actions/Code/CSharp/Available-Methods/OBS)
* [<img src="https://streamer.bot/img/integrations/streamlabs.png"> **StreamLabs Desktop**](/Sub-Actions/Code/CSharp/Available-Methods/StreamLabs-Desktop)
{.btn-grid .my-5}

## Intergrations
* [<img src="https://streamer.bot/img/integrations/voicemod.png"> **VoiceMod**](/Sub-Actions/Code/CSharp/Available-Methods/VoiceMod)
* [<img src="https://streamer.bot/img/integrations/lumia.png"> **Lumia Stream**](/Sub-Actions/Code/CSharp/Available-Methods/Lumia-Stream)
* [<i class="mdi mdi-discord text--discord"></i> **Discord**](/Sub-Actions/Code/CSharp/Available-Methods/Discord)
{.btn-grid .my-5}

# YouTube
## Chat Message

```csharp
void SendYouTubeMessage(string message);
```

## User Variables

```csharp
T GetTwitchUserVar<T>(string userName, string varName, bool persisted = true);
T GetYouTubeUserVar<T>(string userName, string varName, bool persisted = true);
void SetTwitchUserVar(string userName, string varName, object value, bool persisted = true);
void SetYouTubeUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetTwitchUserVar(string userName, string varName, bool persisted = true);
void UnsetYouTubeUserVar(string userName, string varName, bool persisted = true);
void UnsetTwitchUser(string userName, bool persisted = true);
void UnsetYouTubeUser(string userName, bool persisted = true);
```

# OBS
## Connection
```csharp
bool ObsIsConnected(int connection = 0);
bool ObsConnect(int connection = 0);
void ObsDisconnect(int connection = 0);
```

## Stream/Recording Status
```csharp
bool ObsIsStreaming(int connection = 0);
void ObsStopStreaming(int connection = 0);
bool ObsIsRecording(int connection = 0);
void ObsStartRecording(int connection = 0);
void ObsStopRecording(int connection = 0);
void ObsPauseRecording(int connection = 0);
void ObsResumeRecording(int connection = 0);
```

## Scenes
```csharp
void ObsSetScene(string sceneName, int connection = 0);
string ObsGetCurrentScene(int connection = 0);
```

## Sources
```csharp
bool ObsIsSourceVisible(string scene, string source, int connection = 0);
void ObsSetSourceVisibility(string scene, string source, bool visible, int connection = 0);
void ObsShowSource(string scene, string source, int connection = 0);
void ObsHideSource(string scene, string source, int connection = 0);
void ObsHideGroupsSources(string scene, string groupName, int connection = 0);
string ObsSetRandomGroupSourceVisible(string scene, string groupName, int connection = 0);
List<string> ObsGetGroupSources(string scene, string groupName, int connection = 0);
string ObsGetSceneItemProperties(string scene, string source, int connection = 0);
```

## Browser/Text Sources
```csharp
void ObsSetBrowserSource(string scene, string source, string url, int connection = 0);
```
```csharp
// use '\n' for a new line e.g. line 1\nline 2
void ObsSetGdiText(string scene, string source, string text, int connection = 0);
```

## Filters
```csharp
bool ObsIsFilterEnabled(string scene, string filterName, int connection = 0);
bool ObsIsFilterEnabled(string scene, string source, string filterName, int connection = 0);
void ObsSetFilterState(string scene, string filterName, int state, int connection = 0);
void ObsSetFilterState(string scene, string source, string filterName, int state, int connection = 0);
void ObsShowFilter(string scene, string filterName, int connection = 0);
void ObsShowFilter(string scene, string source, string filterName, int connection = 0);
void ObsHideFilter(string scene, string filterName, int connection = 0);
void ObsHideFilter(string scene, string source, string filterName, int connection = 0);
void ObsToggleFilter(string scene, string filterName, int connection = 0);
void ObsToggleFilter(string scene, string source, string filterName, int connection = 0);
void ObsSetRandomFilterState(string scene, int state, int connection = 0);
void ObsSetRandomFilterState(string scene, string source, int state, int connection = 0);
```

## Mute
```csharp
void ObsSetSourceMuteState(string scene, string source, int state, int connection = 0);
void ObsSourceMute(string scene, string source, string filterName, int connection = 0);
void ObsSourceUnMute(string scene, string source, string filterName, int connection = 0);
void ObsSourceMuteToggle(string scene, string source, string filterName, int connection = 0);
```

## Raw
```csharp
string ObsSendRaw(string requestType, string data, int connection = 0);
```

## Hide All Scene/Source Filters
```csharp
void ObsHideSourcesFilters(string scene, string source, int connection = 0);
void ObsHideScenesFilters(string scene, int connection = 0);
```

## Media
```csharp
void ObsSetMediaState(string scene, string source, int state, int connection = 0);
void ObsMediaPlay(string scene, string source, int connection = 0);
void ObsMediaPause(string scene, string source, int connection = 0);
void ObsMediaRestart(string scene, string source, int connection = 0);
void ObsMediaStop(string scene, string source, int connection = 0);
void ObsMediaNext(string scene, string source, int connection = 0);
void ObsMediaPrevious(string scene, string source, int connection = 0);
```

## Colors
```csharp
long ObsConvertRgb(int a, int r, int g, int b);
long ObsConvertColorHex(string colorHex);
```

> Requires a minimum of v0.1.14
{.is-info}

```csharp
void ObsSetColorSourceColor(string scene, string source, int a, int r, int g, int b, int connection = 0);
void ObsSetColorSourceColor(string scene, string source, string hexColor, int connection = 0);
void ObsSetColorSourceRandomColor(string scene, string source, int connection = 0);
```

## Get Connection By Name
```csharp
int ObsGetConnectionByName(string name);
```

## Replay Buffer
```csharp
void ObsSetReplayBufferState(int state, int connection = 0);
void ObsReplayBufferStart(int connection = 0);
void ObsReplayBufferStop(int connection = 0);
void ObsReplayBufferSave(int connection = 0);
```

## Set Media Source File
```csharp
void ObsSetMediaSourceFile(string scene, string source, string file, int connection = 0);
```

## Set Image Source File
```csharp
void ObsSetImageSourceFile(string scene, string source, string file, int connection = 0);
```

## Screenshot
> Requires a minimum of v0.1.14
{.is-info}
```csharp
bool ObsTakeScreenshot(string scene, string source, string path, int quality = -1, int connection = 0);
```

# StreamLabs Desktop
## Connection
```csharp
bool SlobsIsConnected(int connection = 0);
bool SlobsConnect(int connection = 0);
void SlobsDisconnect(int connection = 0);
```

## Stream/Recording Status
```csharp
bool SlobsIsStreaming(int connection = 0);
void SlobsStopStreaming(int connection = 0);
void SlobsStartStreaming(int connection = 0);
bool SlobsIsRecording(int connection = 0);
void SlobsStartRecording(int connection = 0);
void SlobsStopRecording(int connection = 0);
void SlobsPauseRecording(int connection = 0);
void SlobsResumeRecording(int connection = 0);
```

## Scenes
```csharp
void SlobsSetScene(string sceneName, int connection = 0);
string SlobsGetCurrentScene(int connection = 0);
```
## Sources
```csharp
bool SlobsIsSourceVisible(string scene, string source, int connection = 0);
void SlobsSetSourceVisibility(string scene, string source, bool visible, int connection = 0);
void SlobsShowSource(string scene, string source, int connection = 0);
void SlobsHideSource(string scene, string source, int connection = 0);
void SlobsHideGroupsSources(string scene, string groupName, int connection = 0);
string SlobsSetRandomGroupSourceVisible(string scene, string groupName, int connection = 0);
List<string> SlobsGetGroupSources(string scene, string groupName, int connection = 0);
```

## Browser/Text Sources
```csharp
void SlobsSetBrowserSource(string scene, string source, string url, int connection = 0);
void SlobsSetGdiText(string scene, string source, string text, int connection = 0);
```

## Filters
```csharp
bool SlobsIsFilterEnabled(string scene, string filterName, int connection = 0);
bool SlobsIsFilterEnabled(string scene, string source, string filterName, int connection = 0);
void SlobsSetFilterState(string scene, string filterName, int state, int connection = 0);
void SlobsSetFilterState(string scene, string source, string filterName, int state, int connection = 0);
void SlobsShowFilter(string scene, string filterName, int connection = 0);
void SlobsShowFilter(string scene, string source, string filterName, int connection = 0);
void SlobsHideFilter(string scene, string filterName, int connection = 0);
void SlobsHideFilter(string scene, string source, string filterName, int connection = 0);
void SlobsToggleFilter(string scene, string filterName, int connection = 0);
void SlobsToggleFilter(string scene, string source, string filterName, int connection = 0);
void SlobsSetRandomFilterState(string scene, int state, int connection = 0);
void SlobsSetRandomFilterState(string scene, string source, int state, int connection = 0);
```

## Mute
```csharp
void SlobsSetSourceMuteState(string scene, string source, int state, int connection = 0);
void SlobsSourceMute(string scene, string source, string filterName, int connection = 0);
void SlobsSourceUnMute(string scene, string source, string filterName, int connection = 0);
void SlobsSourceMuteToggle(string scene, string source, string filterName, int connection = 0);
```

# Voicemod
## Select Voice
```csharp
void VoiceModSelectVoice(string voiceId);
```

## Voice Changer On/Off
```csharp
bool VoiceModVoiceChangerOn();
bool VoiceModVoiceChangerOff();
```

## Hear My Voice On/Off
```csharp
bool VoiceModHearMyVoiceOn();
bool VoiceModHearMyVoiceOff();
```

## Censor On/Off
```csharp
void VoiceModCensorOn();
void VoiceModCensorOff();
```

## Get Current Voice
```csharp
string VoiceModGetCurrentVoice();
```

## Get Voice Changer Status
```csharp
bool VoiceModGetVoiceChangerStatus();
```

## Get Hear Myself Status
```csharp
bool VoiceModGetHearMyselfStatus();
```

# Lumia Stream
> All of these require a minimum of v0.1.14
{.is-info}
## Set To Default
```csharp
void LumiaSetToDefault();
```

## Send Command
```csharp
void LumiaSendCommand(string command);
```

# Discord
> All of these require a minimum of v0.1.14
{.is-info}
## Post Text To Webhook
```csharp
bool DiscordPostTextToWebhook(string webhookUrl, string content, string username = null, bool textToSpeech = false);
```

---

- [<i class="mdi mdi-chevron-left"></i> **Code *Go Back***](/en/Sub-Actions/Code)
{.btn-grid .my-5}