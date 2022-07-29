---
title: OBS Studio Requests
description: Information on OBS requests that is used in Streamer.bot with OBS raw.
published: true
date: 2022-07-29T19:31:48.990Z
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
* [**GetInputList *Gets an array of all inputs in OBS***](){.disabled}
* [**GetInputKindList *Gets an array of all available input kinds in OBS***](){.disabled}
* [**GetSpecialInputs *Gets the names of all special inputs***](){.disabled}
* [**CreateInput *Creates a new input, adding it as a scene item to the specified scene***](){.disabled}
* [**RemoveInput *Removes an existing input***](){.disabled}
* [**SetInputName *Sets the name of an input (rename)***](){.disabled}
* [**GetInputDefaultSettings *Gets the default settings for an input kind***](){.disabled}
* [**GetInputSettings *Gets the settings of an input***](){.disabled}
* [**SetInputSettings *Sets the settings of an input***](){.disabled}
* [**GetInputMute *Gets the audio mute state of an input***](){.disabled}
* [**SetInputMute *Sets the audio mute state of an input***](){.disabled}
* [**ToggleInputMute *Toggles the audio mute state of an input***](){.disabled}
* [**GetInputVolume *Gets the current volume setting of an input.***](){.disabled}
* [**SetInputVolume *Sets the volume setting of an input***](){.disabled}
* [**GetInputAudioBalance *Gets the audio balance of an input***](){.disabled}
* [**SetInputAudioBalance *Sets the audio balance of an input***](){.disabled}
* [**GetInputAudioSyncOffset *Gets the audio sync offset of an input***](){.disabled}
* [**SetInputAudioSyncOffset *Sets the audio sync offset of an input***](){.disabled}
* [**GetInputAudioMonitorType *Gets the audio monitor type of an input***](){.disabled}
* [**SetInputAudioMonitorType *Sets the audio monitor type of an input***](){.disabled}
* [**GetInputAudioTracks *Gets the enable state of all audio tracks of an input***](){.disabled}
* [**SetInputAudioTracks *Sets the enable state of audio tracks of an input***](){.disabled}
* [**GetInputPropertiesListPropertyItems *Gets the items of a list property from an input's properties***](){.disabled}
* [**PressInputPropertiesButton *Presses a button in the properties of an input***](){.disabled}
{.btn-grid .my-5}

## Transitions Requests
* [**GetTransitionKindList *Gets an array of all available transition kinds***](){.disabled}
* [**GetSceneTransitionList *Gets an array of all scene transitions in OBS***](){.disabled}
* [**GetCurrentSceneTransition *Gets information about the current scene transition***](){.disabled}
* [**SetCurrentSceneTransition *Sets the current scene transition***](){.disabled}
* [**SetCurrentSceneTransitionDuration *Sets the duration of the current scene transition, if it is not fixed***](){.disabled}
* [**SetCurrentSceneTransitionSettings *Sets the settings of the current scene transition***](){.disabled}
* [**GetCurrentSceneTransitionCursor *Gets the cursor position of the current scene transition***](){.disabled}
* [**TriggerStudioModeTransition *Triggers the current scene transition. Same functionality as the Transition button in studio mode***](){.disabled}
* [**SetTBarPosition *Sets the position of the TBar***](){.disabled}
{.btn-grid .my-5}

## Filters Requests
* [**GetSourceFilterList *Gets an array of all of a source's filters***](){.disabled}
* [**GetSourceFilterDefaultSettings *Gets the default settings for a filter kind***](){.disabled}
* [**CreateSourceFilter *Creates a new filter, adding it to the specified source***](){.disabled}
* [**RemoveSourceFilter *Removes a filter from a source***](){.disabled}
* [**SetSourceFilterName *Sets the name of a source filter (rename)***](){.disabled}
* [**GetSourceFilter *Gets the info for a specific source filter***](){.disabled}
* [**SetSourceFilterIndex *Sets the index position of a filter on a source***](){.disabled}
* [**SetSourceFilterSettings *Sets the settings of a source filter***](){.disabled}
* [**SetSourceFilterEnabled *Sets the enable state of a source filter***](){.disabled}
{.btn-grid .my-5}

## Scene Items Requests
* [**GetSceneItemList *Gets a list of all scene items in a scene***](){.disabled}
* [**GetGroupSceneItemList *Basically GetSceneItemList, but for groups***](){.disabled}
* [**GetSceneItemId *Searches a scene for a source, and returns its id***](){.disabled}
* [**CreateSceneItem *Creates a new scene item using a source***](){.disabled}
* [**RemoveSceneItem *Removes a scene item from a scene***](){.disabled}
* [**DuplicateSceneItem *Duplicates a scene item, copying all transform and crop info***](){.disabled}
* [**GetSceneItemTransform *Gets the transform and crop info of a scene item***](){.disabled}
* [**SetSceneItemTransform *Sets the transform and crop info of a scene item***](){.disabled}
* [**GetSceneItemEnabled *Gets the enable state of a scene item***](){.disabled}
* [**SetSceneItemEnabled *Sets the enable state of a scene item***](){.disabled}
* [**GetSceneItemLocked *Gets the lock state of a scene item***](){.disabled}
* [**SetSceneItemLocked *Sets the lock state of a scene item***](){.disabled}
* [**GetSceneItemIndex *Gets the index position of a scene item in a scene***](){.disabled}
* [**SetSceneItemIndex *Sets the index position of a scene item in a scene***](){.disabled}
* [**GetSceneItemBlendMode *Gets the blend mode of a scene item***](){.disabled}
* [**SetSceneItemBlendMode *Sets the blend mode of a scene item***](){.disabled}
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