---
title: C# Available Methods (Coming Soon)
description: Reference of all methods that can be accessed via the CPH object available in Streamer.bot
published: false
date: 2022-10-29T20:56:24.186Z
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
* [<img src="https://streamer.bot/img/integrations/obs.svg"> **OBS Studio**](/Sub-Actions/Code/CSharp/Available-Methods/OBS)
* [<img src="https://streamer.bot/img/integrations/streamlabs.png"> **StreamLabs Desktop**](/Sub-Actions/Code/CSharp/Available-Methods/StreamLabs-Desktop)
{.btn-grid .my-5}

## Intergrations
* [<img src="https://streamer.bot/img/integrations/voicemod.png"> **VoiceMod**](/Sub-Actions/Code/CSharp/Available-Methods/VoiceMod)
* [<img src="https://streamer.bot/img/integrations/lumia.png"> **Lumia Stream**](/Sub-Actions/Code/CSharp/Available-Methods/Lumia-Stream)
* [<i class="mdi mdi-discord text--discord"></i> **Discord**](/Sub-Actions/Code/CSharp/Available-Methods/Discord)
{.btn-grid .my-5}

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