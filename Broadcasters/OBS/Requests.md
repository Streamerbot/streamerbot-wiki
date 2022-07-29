---
title: OBS Studio Requests
description: Information on OBS requests that is used in Streamer.bot with OBS raw.
published: true
date: 2022-07-29T23:30:59.696Z
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
* [**GetPersistentData *Gets the value of a "slot" from the selected persistent data realm***](/en/Broadcasters/OBS/Requests/Config-Requests/GetPersistentData){.disabled}
* [**SetPersistentData *Sets the value of a "slot" from the selected persistent data realm***](/en/Broadcasters/OBS/Requests/Config-Requests/SetPersistentData){.disabled}
* [**GetSceneCollectionList *Gets an array of all scene collections***](/en/Broadcasters/OBS/Requests/Config-Requests/GetSceneCollectionList/en/Broadcasters/OBS/Requests/Config-Requests/NAME){.disabled}
* [**SetCurrentSceneCollection *Switches to a scene collection.***](/en/Broadcasters/OBS/Requests/Config-Requests/SetCurrentSceneCollection){.disabled}
* [**CreateSceneCollection *Creates a new scene collection, switching to it in the process***](/en/Broadcasters/OBS/Requests/Config-Requests/CreateSceneCollection){.disabled}
* [**GetProfileList *Gets an array of all profiles***](/en/Broadcasters/OBS/Requests/Config-Requests/GetProfileList){.disabled}
* [**SetCurrentProfile *Switches to a profile***](/en/Broadcasters/OBS/Requests/Config-Requests/SetCurrentProfile){.disabled}
* [**CreateProfile *Creates a new profile, switching to it in the process***](/en/Broadcasters/OBS/Requests/Config-Requests/CreateProfile){.disabled}
* [**RemoveProfile *Removes a profile. If the current profile is chosen, it will change to a different profile first***](/en/Broadcasters/OBS/Requests/Config-Requests/RemoveProfile){.disabled}
* [**GetProfileParameter *Gets a parameter from the current profile's configuration***](/en/Broadcasters/OBS/Requests/Config-Requests/GetProfileParameter){.disabled}
* [**SetProfileParameter *Sets the value of a parameter in the current profile's configuration***](/en/Broadcasters/OBS/Requests/Config-Requests/SetProfileParameter){.disabled}
* [**GetVideoSettings *Gets the current video settings***](/en/Broadcasters/OBS/Requests/Config-Requests/GetVideoSettings){.disabled}
* [**SetVideoSettings *Sets the current video settings***](/en/Broadcasters/OBS/Requests/Config-Requests/SetVideoSettings){.disabled}
* [**GetStreamServiceSettings *Gets the current stream service settings (stream destination)***](/en/Broadcasters/OBS/Requests/Config-Requests/GetStreamServiceSettings){.disabled}
* [**SetStreamServiceSettings *Sets the current stream service settings (stream destination)***](/en/Broadcasters/OBS/Requests/Config-Requests/SetStreamServiceSettings){.disabled}
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
* [**GetVirtualCamStatus *Gets the status of the virtualcam output***](){.disabled}
* [**ToggleVirtualCam *Toggles the state of the virtualcam output***](){.disabled}
* [**StartVirtualCam *Starts the virtualcam output***](){.disabled}
* [**StopVirtualCam *Stops the virtualcam output***](){.disabled}
* [**GetReplayBufferStatus *Gets the status of the replay buffer output***](){.disabled}
* [**ToggleReplayBuffer *Toggles the state of the replay buffer output***](){.disabled}
* [**StartReplayBuffer *Starts the replay buffer output***](){.disabled}
* [**StopReplayBuffer *Stops the replay buffer output***](){.disabled}
* [**SaveReplayBuffer *Saves the contents of the replay buffer output***](){.disabled}
* [**GetLastReplayBufferReplay *Gets the filename of the last replay buffer save file***](){.disabled}
* [**GetOutputList *Gets the list of available outputs***](){.disabled}
* [**GetOutputStatus *Gets the status of an output***](){.disabled}
* [**ToggleOutput *Toggles the status of an output***](){.disabled}
* [**StartOutput *Starts an output***](){.disabled}
* [**StopOutput *Stops an output***](){.disabled}
* [**GetOutputSettings *Gets the settings of an output***](){.disabled}
* [**SetOutputSettings *Sets the settings of an output***](){.disabled}
{.btn-grid .my-5}

## Stream Requests
* [**GetStreamStatus *Gets the status of the stream output***](){.disabled}
* [**ToggleStream *Toggles the status of the stream output***](){.disabled}
* [**StartStream *Starts the stream output***](){.disabled}
* [**StopStream *Stops the stream output***](){.disabled}
* [**SendStreamCaption *Sends CEA-608 caption text over the stream output***](){.disabled}
{.btn-grid .my-5}

## Record Requests
* [**GetRecordStatus *Gets the status of the record output***](){.disabled}
* [**ToggleRecord *Toggles the status of the record output***](){.disabled}
* [**StartRecord *Starts the record output***](){.disabled}
* [**StopRecord *Stops the record output***](){.disabled}
* [**ToggleRecordPause *Toggles pause on the record output***](){.disabled}
* [**PauseRecord *Pauses the record output***](){.disabled}
* [**ResumeRecord *Resumes the record output***](){.disabled}
{.btn-grid .my-5}

## Media Inputs Requests
* [**GetMediaInputStatus *Gets the status of a media input***](){.disabled}
* [**SetMediaInputCursor *Sets the cursor position of a media input***](){.disabled}
* [**OffsetMediaInputCursor *Offsets the current cursor position of a media input by the specified value***](){.disabled}
* [**TriggerMediaInputAction *Triggers an action on a media input***](){.disabled}
{.btn-grid .my-5}

## Ui Requests
* [**GetStudioModeEnabled *Gets whether studio is enabled***](){.disabled}
* [**SetStudioModeEnabled *Enables or disables studio mode***](){.disabled}
* [**OpenInputPropertiesDialog *Opens the properties dialog of an input***](){.disabled}
* [**OpenInputFiltersDialog *Opens the filters dialog of an input***](){.disabled}
* [**OpenInputInteractDialog *Opens the interact dialog of an input***](){.disabled}
* [**GetMonitorList *Gets a list of connected monitors and information about them***](){.disabled}
* [**OpenVideoMixProjector *Opens a projector for a specific output video mix***](){.disabled}
* [**OpenSourceProjector *Opens a projector for a source***](){.disabled}
{.btn-grid .my-5}

---
- [<i class="mdi mdi-share"></i> **Share your examples! *If you have example(s) for these requests you can submit it in #unearthed-arcana on the streamer.bot discord, there is a high change it will come on these pages***](https://discord.gg/RCcH54hWck)
{.btn-grid}
####
- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/en/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid}