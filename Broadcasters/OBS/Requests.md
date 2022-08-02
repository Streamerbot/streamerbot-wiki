---
title: OBS Studio Requests
description: Information on OBS requests that is used in Streamer.bot with OBS raw.
published: true
date: 2022-08-02T06:32:01.903Z
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
* [**GetVersion *Gets data about the current plugin and RPC version***](/en/Broadcasters/OBS/Requests/General-Requests/GetVersion)
* [**GetStats *Gets statistics about OBS, obs-websocket, and the current session***](/en/Broadcasters/OBS/Requests/General-Requests/GetStats)
* [**BroadcastCustomEvent *Broadcasts a `CustomEvent` to all WebSocket clients. Receivers are clients which are identified and subscribed***](/en/Broadcasters/OBS/Requests/General-Requests/BroadcastCustomEvent){.disabled}
* [**CallVendorRequest *Call a request registered to a vendor***](/en/Broadcasters/OBS/Requests/General-Requests/CallVendorRequest){.disabled}
* [**GetHotkeyList *Gets an array of all hotkey names in OBS***](/en/Broadcasters/OBS/Requests/General-Requests/GetHotkeyList)
* [**TriggerHotkeyByName *Triggers a hotkey using its name. See `GetHotkeyList`***](/en/Broadcasters/OBS/Requests/General-Requests/TriggerHotkeyByName)
* [**TriggerHotkeyByKeySequence *Triggers a hotkey using a sequence of keys***](/en/Broadcasters/OBS/Requests/General-Requests/TriggerHotkeyByKeySequence)
* [**Sleep *Sleeps for a time duration or number of frames. Only available in request batches with types `SERIAL_REALTIME` or `SERIAL_FRAME`***](/en/Broadcasters/OBS/Requests/General-Requests/Sleep){.disabled}
{.btn-grid .my-5}

## Config Requests
* [**GetPersistentData *Gets the value of a "slot" from the selected persistent data realm***](/en/Broadcasters/OBS/Requests/Config-Requests/GetPersistentData){.disabled}
* [**SetPersistentData *Sets the value of a "slot" from the selected persistent data realm***](/en/Broadcasters/OBS/Requests/Config-Requests/SetPersistentData){.disabled}
* [**GetSceneCollectionList *Gets an array of all scene collections***](/en/Broadcasters/OBS/Requests/Config-Requests/GetSceneCollectionList/en/Broadcasters/OBS/Requests/Config-Requests/GetSceneCollectionList)
* [**SetCurrentSceneCollection *Switches to a scene collection.***](/en/Broadcasters/OBS/Requests/Config-Requests/SetCurrentSceneCollection)
* [**CreateSceneCollection *Creates a new scene collection, switching to it in the process***](/en/Broadcasters/OBS/Requests/Config-Requests/CreateSceneCollection)
* [**GetProfileList *Gets an array of all profiles***](/en/Broadcasters/OBS/Requests/Config-Requests/GetProfileList)
* [**SetCurrentProfile *Switches to a profile***](/en/Broadcasters/OBS/Requests/Config-Requests/SetCurrentProfile)
* [**CreateProfile *Creates a new profile, switching to it in the process***](/en/Broadcasters/OBS/Requests/Config-Requests/CreateProfile)
* [**RemoveProfile *Removes a profile. If the current profile is chosen, it will change to a different profile first***](/en/Broadcasters/OBS/Requests/Config-Requests/RemoveProfile)
* [**GetProfileParameter *Gets a parameter from the current profile's configuration***](/en/Broadcasters/OBS/Requests/Config-Requests/GetProfileParameter){.disabled}
* [**SetProfileParameter *Sets the value of a parameter in the current profile's configuration***](/en/Broadcasters/OBS/Requests/Config-Requests/SetProfileParameter){.disabled}
* [**GetVideoSettings *Gets the current video settings***](/en/Broadcasters/OBS/Requests/Config-Requests/GetVideoSettings)
* [**SetVideoSettings *Sets the current video settings***](/en/Broadcasters/OBS/Requests/Config-Requests/SetVideoSettings)
* [**GetStreamServiceSettings *Gets the current stream service settings (stream destination)***](/en/Broadcasters/OBS/Requests/Config-Requests/GetStreamServiceSettings)
* [**SetStreamServiceSettings *Sets the current stream service settings (stream destination)***](/en/Broadcasters/OBS/Requests/Config-Requests/SetStreamServiceSettings)
{.btn-grid .my-5}

## Source Requests
Requests related to sources{.subtitle}
* [**GetSourceActive *Gets the active and show state of a source***](/en/Broadcasters/OBS/Requests/Source-Requests/GetSourceActive)
* [**GetSourceScreenshot *Gets a Base64-encoded screenshot of a source***](/en/Broadcasters/OBS/Requests/Source-Requests/GetSourceScreenshot)
* [**SaveSourceScreenshot *Saves a screenshot of a source to the filesystem***](/en/Broadcasters/OBS/Requests/Source-Requests/SaveSourceScreenshot)
{.btn-grid .my-5}

## Scene Requests
* [**GetSceneList *Gets an array of all scenes in OBS***](/en/Broadcasters/OBS/Requests/Scene-Requests/GetSceneList)
* [**GetGroupList *Gets an array of all groups in OBS***](/en/Broadcasters/OBS/Requests/Scene-Requests/GetGroupList)
* [**GetCurrentProgramScene *Gets the current program scene***](/en/Broadcasters/OBS/Requests/Scene-Requests/GetCurrentProgramScene)
* [**SetCurrentProgramScene *Sets the current program scene***](/en/Broadcasters/OBS/Requests/Scene-Requests/SetCurrentProgramScene)
* [**GetCurrentPreviewScene *Gets the current preview scene***](/en/Broadcasters/OBS/Requests/Scene-Requests/GetCurrentPreviewScene)
* [**SetCurrentPreviewScene *Sets the current preview scene***](/en/Broadcasters/OBS/Requests/Scene-Requests/SetCurrentPreviewScene)
* [**CreateScene *Creates a new scene in OBS***](/en/Broadcasters/OBS/Requests/Scene-Requests/CreateScene)
* [**RemoveScene *Removes a scene from OBS***](/en/Broadcasters/OBS/Requests/Scene-Requests/RemoveScene)
* [**SetSceneName *Sets the name of a scene (rename)***](/en/Broadcasters/OBS/Requests/Scene-Requests/SetSceneName)
* [**GetSceneSceneTransitionOverride *Gets the scene transition overridden for a scene***](/en/Broadcasters/OBS/Requests/Scene-Requests/GetSceneSceneTransitionOverride)
* [**SetSceneSceneTransitionOverride *Gets the scene transition overridden for a scene***](/en/Broadcasters/OBS/Requests/Scene-Requests/SetSceneSceneTransitionOverride)
{.btn-grid .my-5}

## Input Requests
* [**GetInputList *Gets an array of all inputs in OBS***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputList)
* [**GetInputKindList *Gets an array of all available input kinds in OBS***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputKindList)
* [**GetSpecialInputs *Gets the names of all special inputs***](/en/Broadcasters/OBS/Requests/Input-Requests/GetSpecialInputs)
* [**CreateInput *Creates a new input, adding it as a scene item to the specified scene***](/en/Broadcasters/OBS/Requests/Input-Requests/CreateInput)
* [**RemoveInput *Removes an existing input***](/en/Broadcasters/OBS/Requests/Input-Requests/RemoveInput)
* [**SetInputName *Sets the name of an input (rename)***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputName)
* [**GetInputDefaultSettings *Gets the default settings for an input kind***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputDefaultSettings)
* [**GetInputSettings *Gets the settings of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputSettings)
* [**SetInputSettings *Sets the settings of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputSettings)
* [**GetInputMute *Gets the audio mute state of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputMute)
* [**SetInputMute *Sets the audio mute state of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputMute)
* [**ToggleInputMute *Toggles the audio mute state of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/ToggleInputMute)
* [**GetInputVolume *Gets the current volume setting of an input.***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputVolume)
* [**SetInputVolume *Sets the volume setting of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputVolume)
* [**GetInputAudioBalance *Gets the audio balance of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioBalance)
* [**SetInputAudioBalance *Sets the audio balance of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioBalance)
* [**GetInputAudioSyncOffset *Gets the audio sync offset of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioSyncOffset){.disabled}
* [**SetInputAudioSyncOffset *Sets the audio sync offset of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioSyncOffset){.disabled}
* [**GetInputAudioMonitorType *Gets the audio monitor type of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioMonitorType){.disabled}
* [**SetInputAudioMonitorType *Sets the audio monitor type of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioMonitorType){.disabled}
* [**GetInputAudioTracks *Gets the enable state of all audio tracks of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioTracks){.disabled}
* [**SetInputAudioTracks *Sets the enable state of audio tracks of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioTracks){.disabled}
* [**GetInputPropertiesListPropertyItems *Gets the items of a list property from an input's properties***](/en/Broadcasters/OBS/Requests/Input-Requests/GetInputPropertiesListPropertyItems){.disabled}
* [**PressInputPropertiesButton *Presses a button in the properties of an input***](/en/Broadcasters/OBS/Requests/Input-Requests/PressInputPropertiesButton){.disabled}
{.btn-grid .my-5}

## Transition Requests
* [**GetTransitionKindList *Gets an array of all available transition kinds***](/en/Broadcasters/OBS/Requests/Transition-Requests/GetTransitionKindList){.disabled}
* [**GetSceneTransitionList *Gets an array of all scene transitions in OBS***](/en/Broadcasters/OBS/Requests/Transition-Requests/GetSceneTransitionList){.disabled}
* [**GetCurrentSceneTransition *Gets information about the current scene transition***](/en/Broadcasters/OBS/Requests/Transition-Requests/GetCurrentSceneTransition){.disabled}
* [**SetCurrentSceneTransition *Sets the current scene transition***](/en/Broadcasters/OBS/Requests/Transition-Requests/SetCurrentSceneTransition){.disabled}
* [**SetCurrentSceneTransitionDuration *Sets the duration of the current scene transition, if it is not fixed***](/en/Broadcasters/OBS/Requests/Transition-Requests/SetCurrentSceneTransitionDuration){.disabled}
* [**SetCurrentSceneTransitionSettings *Sets the settings of the current scene transition***](/en/Broadcasters/OBS/Requests/Transition-Requests/SetCurrentSceneTransitionSettings){.disabled}
* [**GetCurrentSceneTransitionCursor *Gets the cursor position of the current scene transition***](/en/Broadcasters/OBS/Requests/Transition-Requests/GetCurrentSceneTransitionCursor){.disabled}
* [**TriggerStudioModeTransition *Triggers the current scene transition. Same functionality as the Transition button in studio mode***](/en/Broadcasters/OBS/Requests/Transition-Requests/TriggerStudioModeTransition){.disabled}
* [**SetTBarPosition *Sets the position of the TBar***](/en/Broadcasters/OBS/Requests/Transition-Requests/SetTBarPosition){.disabled}
{.btn-grid .my-5}

## Filter Requests
* [**GetSourceFilterList *Gets an array of all of a source's filters***](/en/Broadcasters/OBS/Requests/Filter-Requests/GetSourceFilterList){.disabled}
* [**GetSourceFilterDefaultSettings *Gets the default settings for a filter kind***](/en/Broadcasters/OBS/Requests/Filter-Requests/GetSourceFilterDefaultSettings){.disabled}
* [**CreateSourceFilter *Creates a new filter, adding it to the specified source***](/en/Broadcasters/OBS/Requests/Filter-Requests/CreateSourceFilter){.disabled}
* [**RemoveSourceFilter *Removes a filter from a source***](/en/Broadcasters/OBS/Requests/Filter-Requests/RemoveSourceFilter){.disabled}
* [**SetSourceFilterName *Sets the name of a source filter (rename)***](/en/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterName){.disabled}
* [**GetSourceFilter *Gets the info for a specific source filter***](/en/Broadcasters/OBS/Requests/Filter-Requests/GetSourceFilter){.disabled}
* [**SetSourceFilterIndex *Sets the index position of a filter on a source***](/en/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterIndex){.disabled}
* [**SetSourceFilterSettings *Sets the settings of a source filter***](/en/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterSettings){.disabled}
* [**SetSourceFilterEnabled *Sets the enable state of a source filter***](/en/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterEnabled){.disabled}
{.btn-grid .my-5}

## Scene Item Requests
* [**GetSceneItemList *Gets a list of all scene items in a scene***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemList){.disabled}
* [**GetGroupSceneItemList *Basically GetSceneItemList, but for groups***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetGroupSceneItemList){.disabled}
* [**GetSceneItemId *Searches a scene for a source, and returns its id***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/){.disabled}
* [**CreateSceneItem *Creates a new scene item using a source***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemId){.disabled}
* [**RemoveSceneItem *Removes a scene item from a scene***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/RemoveSceneItem){.disabled}
* [**DuplicateSceneItem *Duplicates a scene item, copying all transform and crop info***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/DuplicateSceneItem){.disabled}
* [**GetSceneItemTransform *Gets the transform and crop info of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemTransform){.disabled}
* [**SetSceneItemTransform *Sets the transform and crop info of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemTransform){.disabled}
* [**GetSceneItemEnabled *Gets the enable state of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemEnabled){.disabled}
* [**SetSceneItemEnabled *Sets the enable state of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemEnabled){.disabled}
* [**GetSceneItemLocked *Gets the lock state of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemLocked){.disabled}
* [**SetSceneItemLocked *Sets the lock state of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemLocked){.disabled}
* [**GetSceneItemIndex *Gets the index position of a scene item in a scene***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemIndex){.disabled}
* [**SetSceneItemIndex *Sets the index position of a scene item in a scene***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemIndex){.disabled}
* [**GetSceneItemBlendMode *Gets the blend mode of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemBlendMode){.disabled}
* [**SetSceneItemBlendMode *Sets the blend mode of a scene item***](/en/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemBlendMode){.disabled}
{.btn-grid .my-5}

## Output Requests
* [**GetVirtualCamStatus *Gets the status of the virtualcam output***](/en/Broadcasters/OBS/Requests/Output-Requests/GetVirtualCamStatus){.disabled}
* [**ToggleVirtualCam *Toggles the state of the virtualcam output***](/en/Broadcasters/OBS/Requests/Output-Requests/ToggleVirtualCam){.disabled}
* [**StartVirtualCam *Starts the virtualcam output***](/en/Broadcasters/OBS/Requests/Output-Requests/StartVirtualCam){.disabled}
* [**StopVirtualCam *Stops the virtualcam output***](/en/Broadcasters/OBS/Requests/Output-Requests/StopVirtualCam){.disabled}
* [**GetReplayBufferStatus *Gets the status of the replay buffer output***](/en/Broadcasters/OBS/Requests/Output-Requests/GetReplayBufferStatus){.disabled}
* [**ToggleReplayBuffer *Toggles the state of the replay buffer output***](/en/Broadcasters/OBS/Requests/Output-Requests/ToggleReplayBuffer){.disabled}
* [**StartReplayBuffer *Starts the replay buffer output***](/en/Broadcasters/OBS/Requests/Output-Requests/StartReplayBuffer){.disabled}
* [**StopReplayBuffer *Stops the replay buffer output***](/en/Broadcasters/OBS/Requests/Output-Requests/StopReplayBuffer){.disabled}
* [**SaveReplayBuffer *Saves the contents of the replay buffer output***](/en/Broadcasters/OBS/Requests/Output-Requests/){.disabled}
* [**GetLastReplayBufferReplay *Gets the filename of the last replay buffer save file***](/en/Broadcasters/OBS/Requests/Output-Requests/GetLastReplayBufferReplay){.disabled}
* [**GetOutputList *Gets the list of available outputs***](/en/Broadcasters/OBS/Requests/Output-Requests/GetOutputList){.disabled}
* [**GetOutputStatus *Gets the status of an output***](/en/Broadcasters/OBS/Requests/Output-Requests/GetOutputStatus){.disabled}
* [**ToggleOutput *Toggles the status of an output***](/en/Broadcasters/OBS/Requests/Output-Requests/ToggleOutput){.disabled}
* [**StartOutput *Starts an output***](/en/Broadcasters/OBS/Requests/Output-Requests/StartOutput){.disabled}
* [**StopOutput *Stops an output***](/en/Broadcasters/OBS/Requests/Output-Requests/StopOutput){.disabled}
* [**GetOutputSettings *Gets the settings of an output***](/en/Broadcasters/OBS/Requests/Output-Requests/GetOutputSettings){.disabled}
* [**SetOutputSettings *Sets the settings of an output***](/en/Broadcasters/OBS/Requests/Output-Requests/SetOutputSettings){.disabled}
{.btn-grid .my-5}

## Stream Requests
* [**GetStreamStatus *Gets the status of the stream output***](/en/Broadcasters/OBS/Requests/Stream-Requests/GetStreamStatus){.disabled}
* [**ToggleStream *Toggles the status of the stream output***](/en/Broadcasters/OBS/Requests/Stream-Requests/ToggleStream){.disabled}
* [**StartStream *Starts the stream output***](/en/Broadcasters/OBS/Requests/Stream-Requests/StartStream){.disabled}
* [**StopStream *Stops the stream output***](/en/Broadcasters/OBS/Requests/Stream-Requests/StopStream){.disabled}
* [**SendStreamCaption *Sends CEA-608 caption text over the stream output***](/en/Broadcasters/OBS/Requests/Stream-Requests/SendStreamCaption){.disabled}
{.btn-grid .my-5}

## Record Requests
* [**GetRecordStatus *Gets the status of the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/GetRecordStatus){.disabled}
* [**ToggleRecord *Toggles the status of the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/ToggleRecord){.disabled}
* [**StartRecord *Starts the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/StartRecord){.disabled}
* [**StopRecord *Stops the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/StopRecord){.disabled}
* [**ToggleRecordPause *Toggles pause on the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/ToggleRecordPause){.disabled}
* [**PauseRecord *Pauses the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/PauseRecord){.disabled}
* [**ResumeRecord *Resumes the record output***](/en/Broadcasters/OBS/Requests/Record-Requests/ResumeRecord){.disabled}
{.btn-grid .my-5}

## Media Input Requests
* [**GetMediaInputStatus *Gets the status of a media input***](/en/Broadcasters/OBS/Requests/Media-Input-Requests/GetMediaInputStatus){.disabled}
* [**SetMediaInputCursor *Sets the cursor position of a media input***](/en/Broadcasters/OBS/Requests/Media-Input-Requests/SetMediaInputCursor){.disabled}
* [**OffsetMediaInputCursor *Offsets the current cursor position of a media input by the specified value***](/en/Broadcasters/OBS/Requests/Media-Input-Requests/OffsetMediaInputCursor){.disabled}
* [**TriggerMediaInputAction *Triggers an action on a media input***](/en/Broadcasters/OBS/Requests/Media-Input-Requests/TriggerMediaInputAction){.disabled}
{.btn-grid .my-5}

## Ui Requests
* [**GetStudioModeEnabled *Gets whether studio is enabled***](/en/Broadcasters/OBS/Requests/Ui-Requests/GetStudioModeEnabled){.disabled}
* [**SetStudioModeEnabled *Enables or disables studio mode***](/en/Broadcasters/OBS/Requests/Ui-Requests/SetStudioModeEnabled){.disabled}
* [**OpenInputPropertiesDialog *Opens the properties dialog of an input***](/en/Broadcasters/OBS/Requests/Ui-Requests/OpenInputPropertiesDialog){.disabled}
* [**OpenInputFiltersDialog *Opens the filters dialog of an input***](/en/Broadcasters/OBS/Requests/Ui-Requests/OpenInputFiltersDialog){.disabled}
* [**OpenInputInteractDialog *Opens the interact dialog of an input***](/en/Broadcasters/OBS/Requests/Ui-Requests/OpenInputInteractDialog){.disabled}
* [**GetMonitorList *Gets a list of connected monitors and information about them***](/en/Broadcasters/OBS/Requests/Ui-Requests/GetMonitorList){.disabled}
* [**OpenVideoMixProjector *Opens a projector for a specific output video mix***](/en/Broadcasters/OBS/Requests/Ui-Requests/OpenVideoMixProjector){.disabled}
* [**OpenSourceProjector *Opens a projector for a source***](/en/Broadcasters/OBS/Requests/Ui-Requests/OpenSourceProjector){.disabled}
{.btn-grid .my-5}

---
- [<i class="mdi mdi-share"></i> **Share your examples! *If you have example(s) for these requests you can submit it in #unearthed-arcana on the streamer.bot discord, there is a high change it will come on these pages***](https://discord.gg/RCcH54hWck)
{.btn-grid}
####
- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/en/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid}