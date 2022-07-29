---
title: OBS Studio Requests
description: Information on OBS requests that is used in Streamer.bot with OBS raw.
published: true
date: 2022-07-29T19:12:09.364Z
tags: 
editor: markdown
dateCreated: 2022-07-19T18:29:42.792Z
---

> All these events won't exist yet, because streamer.bot is currently on OBS websocket *v4.x.x*{.version-badge} 
> Event Title `White` = `Page exist`
> Event Title `Gray` = `Page doesn't exist`
{.is-danger}

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## General Requests
* [**GetVersion *Gets data about the current plugin and RPC version***](/en/Broadcasters/OBS/Requests/General-Requests/GetVersion){.disabled}
* [**GetStats *Gets statistics about OBS, obs-websocket, and the current session***](/en/Broadcasters/OBS/Requests/General-Requests/GetStats){.disabled}
* [**BroadcastCustomEvent *Broadcasts a `CustomEvent` to all WebSocket clients. Receivers are clients which are identified and subscribed***](/en/Broadcasters/OBS/Requests/General-Requests/BroadcastCustomEvent){.disabled}
* [**CallVendorRequest *Call a request registered to a vendor***](/en/Broadcasters/OBS/Requests/General-Requests/CallVendorRequest){.disabled}
* [**GetHotkeyList *Gets an array of all hotkey names in OBS***](/en/Broadcasters/OBS/Requests/General-Requests/GetHotkeyList){.disabled}
* [**TriggerHotkeyByName *Triggers a hotkey using its name. See `GetHotkeyList`***](/en/Broadcasters/OBS/Requests/General-Requests/TriggerHotkeyByName){.disabled}
* [**TriggerHotkeyByKeySequence *Triggers a hotkey using a sequence of keys***](/en/Broadcasters/OBS/Requests/General-Requests/TriggerHotkeyByKeySequence){.disabled}
* [**Sleep *Sleeps for a time duration or number of frames. Only available in request batches with types `SERIAL_REALTIME` or `SERIAL_FRAME`***](/en/Broadcasters/OBS/Requests/General-Requests/Sleep){.disabled}
{.btn-grid .my-5}

## Config Requests
* [**GetPersistentData *Gets the value of a "slot" from the selected persistent data realm***](){.disabled}
* [**SetPersistentData *Sets the value of a "slot" from the selected persistent data realm***](){.disabled}
* [**GetSceneCollectionList *Gets an array of all scene collections***](){.disabled}
* [**SetCurrentSceneCollection *Switches to a scene collection.***](){.disabled}
* [**CreateSceneCollection *Creates a new scene collection, switching to it in the process***](){.disabled}
* [**GetProfileList *Gets an array of all profiles***](){.disabled}
* [**SetCurrentProfile *Switches to a profile***](){.disabled}
* [**CreateProfile *Creates a new profile, switching to it in the process***](){.disabled}
* [**RemoveProfile *Removes a profile. If the current profile is chosen, it will change to a different profile first***](){.disabled}
* [**GetProfileParameter *Gets a parameter from the current profile's configuration***](){.disabled}
* [**SetProfileParameter *Sets the value of a parameter in the current profile's configuration***](){.disabled}
* [**GetVideoSettings *Gets the current video settings***](){.disabled}
* [**SetVideoSettings *Sets the current video settings***](){.disabled}
* [**GetStreamServiceSettings *Gets the current stream service settings (stream destination)***](){.disabled}
* [**SetStreamServiceSettings *Sets the current stream service settings (stream destination)***](){.disabled}
{.btn-grid .my-5}

## Sources Requests
* [**GetSourceActive *Gets the active and show state of a source***](){.disabled}
* [**GetSourceScreenshot *Gets a Base64-encoded screenshot of a source***](){.disabled}
* [**SaveSourceScreenshot *Saves a screenshot of a source to the filesystem***](){.disabled}
{.btn-grid .my-5}

## Scenes Requests
* [**GetSceneList *Gets an array of all scenes in OBS***](){.disabled}
* [**GetGroupList *Gets an array of all groups in OBS***](){.disabled}
* [**GetCurrentProgramScene *Gets the current program scene***](){.disabled}
* [**SetCurrentProgramScene *Sets the current program scene***](){.disabled}
* [**GetCurrentPreviewScene *Gets the current preview scene***](){.disabled}
* [**SetCurrentPreviewScene *Sets the current preview scene***](){.disabled}
* [**CreateScene *Creates a new scene in OBS***](){.disabled}
* [**RemoveScene *Removes a scene from OBS***](){.disabled}
* [**SetSceneName *Sets the name of a scene (rename)***](){.disabled}
* [**GetSceneSceneTransitionOverride *Gets the scene transition overridden for a scene***](){.disabled}
* [**SetSceneSceneTransitionOverride *Gets the scene transition overridden for a scene***](){.disabled}
{.btn-grid .my-5}

## Inputs Requests
* [**GetInputList *Desription***](){.disabled}
* [**GetInputKindList *Desription***](){.disabled}
* [**GetSpecialInputs *Desription***](){.disabled}
* [**CreateInput *Desription***](){.disabled}
* [**RemoveInput *Desription***](){.disabled}
* [**SetInputName *Desription***](){.disabled}
* [**GetInputDefaultSettings *Desription***](){.disabled}
* [**GetInputSettings *Desription***](){.disabled}
* [**SetInputSettings *Desription***](){.disabled}
* [**GetInputMute *Desription***](){.disabled}
* [**SetInputMute *Desription***](){.disabled}
* [**ToggleInputMute *Desription***](){.disabled}
* [**GetInputVolume *Gets the current volume setting of an input.***](){.disabled}
* [**SetInputVolume *Desription***](){.disabled}
* [**GetInputAudioBalance *Desription***](){.disabled}
* [**SetInputAudioBalance *Desription***](){.disabled}
* [**GetInputAudioSyncOffset *Desription***](){.disabled}
* [**SetInputAudioSyncOffset *Desription***](){.disabled}
* [**GetInputAudioMonitorType *Desription***](){.disabled}
* [**SetInputAudioMonitorType *Desription***](){.disabled}
* [**GetInputAudioTracks *Desription***](){.disabled}
* [**SetInputAudioTracks *Desription***](){.disabled}
* [**GetInputPropertiesListPropertyItems *Desription***](){.disabled}
* [**PressInputPropertiesButton *Desription***](){.disabled}
{.btn-grid .my-5}

## Transitions Requests
* [**GetTransitionKindList *Desription***](){.disabled}
* [**GetSceneTransitionList *Desription***](){.disabled}
* [**GetCurrentSceneTransition *Desription***](){.disabled}
* [**SetCurrentSceneTransition *Desription***](){.disabled}
* [**SetCurrentSceneTransitionDuration *Desription***](){.disabled}
* [**SetCurrentSceneTransitionSettings *Desription***](){.disabled}
* [**GetCurrentSceneTransitionCursor *Desription***](){.disabled}
* [**TriggerStudioModeTransition *Desription***](){.disabled}
* [**SetTBarPosition *Desription***](){.disabled}
{.btn-grid .my-5}

## Filters Requests
* [**GetSourceFilterList *Desription***](){.disabled}
* [**GetSourceFilterDefaultSettings *Desription***](){.disabled}
* [**CreateSourceFilter *Desription***](){.disabled}
* [**RemoveSourceFilter *Desription***](){.disabled}
* [**SetSourceFilterName *Desription***](){.disabled}
* [**GetSourceFilter *Desription***](){.disabled}
* [**SetSourceFilterIndex *Desription***](){.disabled}
* [**SetSourceFilterSettings *Desription***](){.disabled}
* [**SetSourceFilterEnabled *Desription***](){.disabled}
{.btn-grid .my-5}

## Scene Items Requests
* [**GetSceneItemList *Desription***](){.disabled}
* [**GetGroupSceneItemList *Desription***](){.disabled}
* [**GetSceneItemId *Desription***](){.disabled}
* [**CreateSceneItem *Desription***](){.disabled}
* [**RemoveSceneItem *Desription***](){.disabled}
* [**DuplicateSceneItem *Desription***](){.disabled}
* [**GetSceneItemTransform *Desription***](){.disabled}
* [**SetSceneItemTransform *Desription***](){.disabled}
* [**GetSceneItemEnabled *Desription***](){.disabled}
* [**SetSceneItemEnabled *Desription***](){.disabled}
* [**GetSceneItemLocked *Desription***](){.disabled}
* [**SetSceneItemLocked *Desription***](){.disabled}
* [**GetSceneItemIndex *Desription***](){.disabled}
* [**SetSceneItemIndex *Desription***](){.disabled}
* [**GetSceneItemBlendMode *Desription***](){.disabled}
* [**SetSceneItemBlendMode *Desription***](){.disabled}
{.btn-grid .my-5}

## Outputs Requests
* [**GetVirtualCamStatus *Desription***](){.disabled}
* [**ToggleVirtualCam *Desription***](){.disabled}
* [**StartVirtualCam *Desription***](){.disabled}
* [**StopVirtualCam *Desription***](){.disabled}
* [**GetReplayBufferStatus *Desription***](){.disabled}
* [**ToggleReplayBuffer *Desription***](){.disabled}
* [**StartReplayBuffer *Desription***](){.disabled}
* [**StopReplayBuffer *Desription***](){.disabled}
* [**SaveReplayBuffer *Desription***](){.disabled}
* [**GetLastReplayBufferReplay *Desription***](){.disabled}
* [**GetOutputList *Desription***](){.disabled}
* [**GetOutputStatus *Desription***](){.disabled}
* [**ToggleOutput *Desription***](){.disabled}
* [**StopOutput *Desription***](){.disabled}
* [**GetOutputSettings *Desription***](){.disabled}
* [**SetOutputSettings *Desription***](){.disabled}
{.btn-grid .my-5}

## Stream Requests
* [**GetStreamStatus *Desription***](){.disabled}
* [**ToggleStream *Desription***](){.disabled}
* [**StartStream *Desription***](){.disabled}
* [**StopStream *Desription***](){.disabled}
* [**SendStreamCaption *Desription***](){.disabled}
{.btn-grid .my-5}

## Record Requests
* [**GetRecordStatus *Desription***](){.disabled}
* [**ToggleRecord *Desription***](){.disabled}
* [**StartRecord *Desription***](){.disabled}
* [**StopRecord *Desription***](){.disabled}
* [**ToggleRecordPause *Desription***](){.disabled}
* [**PauseRecord *Desription***](){.disabled}
{.btn-grid .my-5}

## Media Inputs Requests
* [**GetMediaInputStatus *Desription***](){.disabled}
* [**SetMediaInputCursor *Desription***](){.disabled}
* [**OffsetMediaInputCursor *Desription***](){.disabled}
* [**TriggerMediaInputAction *Desription***](){.disabled}
{.btn-grid .my-5}

## Ui Requests
* [**GetStudioModeEnabled *Desription***](){.disabled}
* [**SetStudioModeEnabled *Desription***](){.disabled}
* [**OpenInputPropertiesDialog *Desription***](){.disabled}
* [**OpenInputFiltersDialog *Desription***](){.disabled}
* [**OpenInputInteractDialog *Desription***](){.disabled}
* [**GetMonitorList *Desription***](){.disabled}
* [**OpenVideoMixProjector *Desription***](){.disabled}
* [**OpenSourceProjector *Desription***](){.disabled}
{.btn-grid .my-5}

---
- [<i class="mdi mdi-share"></i> **Share your examples! *If you have example(s) for these requests you can submit it in #unearthed-arcana on the streamer.bot discord, there is a high change it will come on these pages***](https://discord.gg/RCcH54hWck)
{.btn-grid}
####
- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/en/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid}