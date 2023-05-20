---
title: OBS Studio
description: C# Available Methods Reference
published: true
date: 2023-05-02T00:12:23.652Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:56:46.806Z
---

## Connection
```csharp
bool ObsIsConnected(int connection = 0);
bool ObsConnect(int connection = 0);
void ObsDisconnect(int connection = 0);
```

```csharp
int ObsGetConnectionByName(string name);
```

## Stream
```csharp
bool ObsIsStreaming(int connection = 0);
void ObsStopStreaming(int connection = 0);
```

## Recording
```csharp
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
void ObsSetSourceVisibility(string scene, string source, bool visible, int connection = 0);
void ObsHideSource(string scene, string source, int connection = 0);
void ObsShowSource(string scene, string source, int connection = 0);

string ObsGetSceneItemProperties(string scene, string source, int connection = 0);
List<string> ObsGetGroupSources(string scene, string groupName, int connection = 0);
bool ObsIsSourceVisible(string scene, string source, int connection = 0);

string ObsSetRandomGroupSourceVisible(string scene, string groupName, int connection = 0);
void ObsHideGroupsSources(string scene, string groupName, int connection = 0);
```

## Browser Sources
```csharp
void ObsSetBrowserSource(string scene, string source, string url, int connection = 0);
```

## GDI+ Text Sources

```csharp
// use '\n' for a new line e.g. line 1\nline 2
void ObsSetGdiText(string scene, string source, string text, int connection = 0);
```

## Filters
```csharp
bool ObsIsFilterEnabled(string scene, string filterName, int connection = 0);
bool ObsIsFilterEnabled(string scene, string source, string filterName, int connection = 0);
```

```csharp
void ObsSetFilterState(string scene, string filterName, int state, int connection = 0);
void ObsSetFilterState(string scene, string source, string filterName, int state, int connection = 0);
```

```csharp
void ObsShowFilter(string scene, string filterName, int connection = 0);
void ObsShowFilter(string scene, string source, string filterName, int connection = 0);
```

```csharp
void ObsHideFilter(string scene, string filterName, int connection = 0);
void ObsHideFilter(string scene, string source, string filterName, int connection = 0);
```

```csharp
void ObsToggleFilter(string scene, string filterName, int connection = 0);
void ObsToggleFilter(string scene, string source, string filterName, int connection = 0);
```

```csharp
void ObsSetRandomFilterState(string scene, int state, int connection = 0);
void ObsSetRandomFilterState(string scene, string source, int state, int connection = 0);
```

## Mute
```csharp
void ObsSetSourceMuteState(string scene, string source, int state, int connection = 0);
void ObsSourceMute(string scene, string source, int connection = 0);
void ObsSourceUnMute(string scene, string source, int connection = 0);
void ObsSourceMuteToggle(string scene, string source, int connection = 0);
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
All `state` enums that are used for `int state` (use the number property on the left side):

----:|:------------
`0` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_NONE` | No action.
`1` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_PLAY` | Play the media input.
`2` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_PAUSE` | Pause the media input.
`3` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_STOP` | Stop the media input.
`4` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_RESTART` | Restart the media input.
`5` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_NEXT` | Go to the next playlist item.
`6` | `OBS_WEBSOCKET_MEDIA_INPUT_ACTION_PREVIOUS` | Go to the previous playlist item.

```csharp
void ObsSetMediaState(string scene, string source, int state, int connection = 0);
```

```csharp
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

```csharp
void ObsSetColorSourceColor(string scene, string source, int a, int r, int g, int b, int connection = 0);
void ObsSetColorSourceColor(string scene, string source, string hexColor, int connection = 0);
void ObsSetColorSourceRandomColor(string scene, string source, int connection = 0);
```

## Replay Buffer
```csharp
void ObsSetReplayBufferState(int state, int connection = 0);
```

```csharp
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
```csharp
bool ObsTakeScreenshot(string scene, string source, string path, int quality = -1, int connection = 0);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}