---
title: OBS Studio Requests v5
description: Information on OBS requests that is used in Streamer.bot with OBS raw.
published: true
date: 2023-03-16T11:26:19.976Z
tags: 
editor: markdown
dateCreated: 2022-07-19T18:29:42.792Z
---

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## Format
This is the format you need to follow with each request{.subtitle}

In the request data you need to fill in the request fields that are shown on each page below
```json
{
  "requestType": "request method",
  "requestData": { ... }
}
```

## General Requests
General & Miscellaneous OBS Studio requests{.subtitle}
* [**GetVersion *Gets data about the current plugin and RPC version***](/Broadcasters/OBS/Requests/General-Requests/GetVersion)
* [**GetStats *Gets statistics about OBS, obs-websocket, and the current session***](/Broadcasters/OBS/Requests/General-Requests/GetStats)
* [**BroadcastCustomEvent *Broadcasts a `CustomEvent` to all WebSocket clients. Receivers are clients which are identified and subscribed***](/Broadcasters/OBS/Requests/General-Requests/BroadcastCustomEvent)
* [**CallVendorRequest *Call a request registered to a vendor***](/Broadcasters/OBS/Requests/General-Requests/CallVendorRequest)
* [**GetHotkeyList *Gets an array of all hotkey names in OBS***](/Broadcasters/OBS/Requests/General-Requests/GetHotkeyList)
* [**TriggerHotkeyByName *Triggers a hotkey using its name. See `GetHotkeyList`***](/Broadcasters/OBS/Requests/General-Requests/TriggerHotkeyByName)
* [**TriggerHotkeyByKeySequence *Triggers a hotkey using a sequence of keys***](/Broadcasters/OBS/Requests/General-Requests/TriggerHotkeyByKeySequence)
* [**Sleep *Sleeps for a time duration or number of frames. Only available in request batches with types `SERIAL_REALTIME` or `SERIAL_FRAME`***](/Broadcasters/OBS/Requests/General-Requests/Sleep)
{.btn-grid .my-5}

## Config Requests
Config related OBS Studio requests{.subtitle}
* [**GetPersistentData *Gets the value of a "slot" from the selected persistent data realm***](/Broadcasters/OBS/Requests/Config-Requests/GetPersistentData)
* [**SetPersistentData *Sets the value of a "slot" from the selected persistent data realm***](/Broadcasters/OBS/Requests/Config-Requests/SetPersistentData)
* [**GetSceneCollectionList *Gets an array of all scene collections***](/Broadcasters/OBS/Requests/Config-Requests/GetSceneCollectionList)
* [**SetCurrentSceneCollection *Switches to a scene collection.***](/Broadcasters/OBS/Requests/Config-Requests/SetCurrentSceneCollection)
* [**CreateSceneCollection *Creates a new scene collection, switching to it in the process***](/Broadcasters/OBS/Requests/Config-Requests/CreateSceneCollection)
* [**GetProfileList *Gets an array of all profiles***](/Broadcasters/OBS/Requests/Config-Requests/GetProfileList)
* [**SetCurrentProfile *Switches to a profile***](/Broadcasters/OBS/Requests/Config-Requests/SetCurrentProfile)
* [**CreateProfile *Creates a new profile, switching to it in the process***](/Broadcasters/OBS/Requests/Config-Requests/CreateProfile)
* [**RemoveProfile *Removes a profile. If the current profile is chosen, it will change to a different profile first***](/Broadcasters/OBS/Requests/Config-Requests/RemoveProfile)
* [**GetProfileParameter *Gets a parameter from the current profile's configuration***](/Broadcasters/OBS/Requests/Config-Requests/GetProfileParameter)
* [**SetProfileParameter *Sets the value of a parameter in the current profile's configuration***](/Broadcasters/OBS/Requests/Config-Requests/SetProfileParameter)
* [**GetVideoSettings *Gets the current video settings***](/Broadcasters/OBS/Requests/Config-Requests/GetVideoSettings)
* [**SetVideoSettings *Sets the current video settings***](/Broadcasters/OBS/Requests/Config-Requests/SetVideoSettings)
* [**GetStreamServiceSettings *Gets the current stream service settings (stream destination)***](/Broadcasters/OBS/Requests/Config-Requests/GetStreamServiceSettings)
* [**SetStreamServiceSettings *Sets the current stream service settings (stream destination)***](/Broadcasters/OBS/Requests/Config-Requests/SetStreamServiceSettings)
{.btn-grid .my-5}

## Source Requests
Source related OBS Studio requests{.subtitle}
* [**GetSourceActive *Gets the active and show state of a source***](/Broadcasters/OBS/Requests/Source-Requests/GetSourceActive)
* [**GetSourceScreenshot *Gets a Base64-encoded screenshot of a source***](/Broadcasters/OBS/Requests/Source-Requests/GetSourceScreenshot)
* [**SaveSourceScreenshot *Saves a screenshot of a source to the filesystem***](/Broadcasters/OBS/Requests/Source-Requests/SaveSourceScreenshot)
{.btn-grid .my-5}

## Scene Requests
Scene related OBS Studio requests{.subtitle}
* [**GetSceneList *Gets an array of all scenes in OBS***](/Broadcasters/OBS/Requests/Scene-Requests/GetSceneList)
* [**GetGroupList *Gets an array of all groups in OBS***](/Broadcasters/OBS/Requests/Scene-Requests/GetGroupList)
* [**GetCurrentProgramScene *Gets the current program scene***](/Broadcasters/OBS/Requests/Scene-Requests/GetCurrentProgramScene)
* [**SetCurrentProgramScene *Sets the current program scene***](/Broadcasters/OBS/Requests/Scene-Requests/SetCurrentProgramScene)
* [**GetCurrentPreviewScene *Gets the current preview scene***](/Broadcasters/OBS/Requests/Scene-Requests/GetCurrentPreviewScene)
* [**SetCurrentPreviewScene *Sets the current preview scene***](/Broadcasters/OBS/Requests/Scene-Requests/SetCurrentPreviewScene)
* [**CreateScene *Creates a new scene in OBS***](/Broadcasters/OBS/Requests/Scene-Requests/CreateScene)
* [**RemoveScene *Removes a scene from OBS***](/Broadcasters/OBS/Requests/Scene-Requests/RemoveScene)
* [**SetSceneName *Sets the name of a scene (rename)***](/Broadcasters/OBS/Requests/Scene-Requests/SetSceneName)
* [**GetSceneSceneTransitionOverride *Gets the scene transition overridden for a scene***](/Broadcasters/OBS/Requests/Scene-Requests/GetSceneSceneTransitionOverride)
* [**SetSceneSceneTransitionOverride *Gets the scene transition overridden for a scene***](/Broadcasters/OBS/Requests/Scene-Requests/SetSceneSceneTransitionOverride)
{.btn-grid .my-5}

## Input Requests
Input related OBS Studio requests{.subtitle}
* [**GetInputList *Gets an array of all inputs in OBS***](/Broadcasters/OBS/Requests/Input-Requests/GetInputList)
* [**GetInputKindList *Gets an array of all available input kinds in OBS***](/Broadcasters/OBS/Requests/Input-Requests/GetInputKindList)
* [**GetSpecialInputs *Gets the names of all special inputs***](/Broadcasters/OBS/Requests/Input-Requests/GetSpecialInputs)
* [**CreateInput *Creates a new input, adding it as a scene item to the specified scene***](/Broadcasters/OBS/Requests/Input-Requests/CreateInput)
* [**RemoveInput *Removes an existing input***](/Broadcasters/OBS/Requests/Input-Requests/RemoveInput)
* [**SetInputName *Sets the name of an input (rename)***](/Broadcasters/OBS/Requests/Input-Requests/SetInputName)
* [**GetInputDefaultSettings *Gets the default settings for an input kind***](/Broadcasters/OBS/Requests/Input-Requests/GetInputDefaultSettings)
* [**GetInputSettings *Gets the settings of an input***](/Broadcasters/OBS/Requests/Input-Requests/GetInputSettings)
* [**SetInputSettings *Sets the settings of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputSettings)
* [**GetInputMute *Gets the audio mute state of an input***](/Broadcasters/OBS/Requests/Input-Requests/GetInputMute)
* [**SetInputMute *Sets the audio mute state of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputMute)
* [**ToggleInputMute *Toggles the audio mute state of an input***](/Broadcasters/OBS/Requests/Input-Requests/ToggleInputMute)
* [**GetInputVolume *Gets the current volume setting of an input.***](/Broadcasters/OBS/Requests/Input-Requests/GetInputVolume)
* [**SetInputVolume *Sets the volume setting of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputVolume)
* [**GetInputAudioBalance *Gets the audio balance of an input***](/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioBalance)
* [**SetInputAudioBalance *Sets the audio balance of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioBalance)
* [**GetInputAudioSyncOffset *Gets the audio sync offset of an input***](/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioSyncOffset)
* [**SetInputAudioSyncOffset *Sets the audio sync offset of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioSyncOffset)
* [**GetInputAudioMonitorType *Gets the audio monitor type of an input***](/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioMonitorType)
* [**SetInputAudioMonitorType *Sets the audio monitor type of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioMonitorType)
* [**GetInputAudioTracks *Gets the enable state of all audio tracks of an input***](/Broadcasters/OBS/Requests/Input-Requests/GetInputAudioTracks)
* [**SetInputAudioTracks *Sets the enable state of audio tracks of an input***](/Broadcasters/OBS/Requests/Input-Requests/SetInputAudioTracks)
* [**GetInputPropertiesListPropertyItems *Gets the items of a list property from an input's properties***](/Broadcasters/OBS/Requests/Input-Requests/GetInputPropertiesListPropertyItems)
* [**PressInputPropertiesButton *Presses a button in the properties of an input***](/Broadcasters/OBS/Requests/Input-Requests/PressInputPropertiesButton)
{.btn-grid .my-5}

## Transition Requests
Transition related OBS Studio requests{.subtitle}
* [**GetTransitionKindList *Gets an array of all available transition kinds***](/Broadcasters/OBS/Requests/Transition-Requests/GetTransitionKindList)
* [**GetSceneTransitionList *Gets an array of all scene transitions in OBS***](/Broadcasters/OBS/Requests/Transition-Requests/GetSceneTransitionList)
* [**GetCurrentSceneTransition *Gets information about the current scene transition***](/Broadcasters/OBS/Requests/Transition-Requests/GetCurrentSceneTransition)
* [**SetCurrentSceneTransition *Sets the current scene transition***](/Broadcasters/OBS/Requests/Transition-Requests/SetCurrentSceneTransition)
* [**SetCurrentSceneTransitionDuration *Sets the duration of the current scene transition, if it is not fixed***](/Broadcasters/OBS/Requests/Transition-Requests/SetCurrentSceneTransitionDuration)
* [**SetCurrentSceneTransitionSettings *Sets the settings of the current scene transition***](/Broadcasters/OBS/Requests/Transition-Requests/SetCurrentSceneTransitionSettings)
* [**GetCurrentSceneTransitionCursor *Gets the cursor position of the current scene transition***](/Broadcasters/OBS/Requests/Transition-Requests/GetCurrentSceneTransitionCursor)
* [**TriggerStudioModeTransition *Triggers the current scene transition. Same functionality as the Transition button in studio mode***](/Broadcasters/OBS/Requests/Transition-Requests/TriggerStudioModeTransition)
* [**SetTBarPosition *Sets the position of the TBar***](/Broadcasters/OBS/Requests/Transition-Requests/SetTBarPosition)
{.btn-grid .my-5}

## Filter Requests
Filter related OBS Studio requests{.subtitle}
* [**GetSourceFilterList *Gets an array of all of a source's filters***](/Broadcasters/OBS/Requests/Filter-Requests/GetSourceFilterList)
* [**GetSourceFilterDefaultSettings *Gets the default settings for a filter kind***](/Broadcasters/OBS/Requests/Filter-Requests/GetSourceFilterDefaultSettings)
* [**CreateSourceFilter *Creates a new filter, adding it to the specified source***](/Broadcasters/OBS/Requests/Filter-Requests/CreateSourceFilter)
* [**RemoveSourceFilter *Removes a filter from a source***](/Broadcasters/OBS/Requests/Filter-Requests/RemoveSourceFilter)
* [**SetSourceFilterName *Sets the name of a source filter (rename)***](/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterName)
* [**GetSourceFilter *Gets the info for a specific source filter***](/Broadcasters/OBS/Requests/Filter-Requests/GetSourceFilter)
* [**SetSourceFilterIndex *Sets the index position of a filter on a source***](/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterIndex)
* [**SetSourceFilterSettings *Sets the settings of a source filter***](/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterSettings)
* [**SetSourceFilterEnabled *Sets the enable state of a source filter***](/Broadcasters/OBS/Requests/Filter-Requests/SetSourceFilterEnabled)
{.btn-grid .my-5}

## Scene Item Requests
Scene Item related OBS Studio requests{.subtitle}
* [**GetSceneItemList *Gets a list of all scene items in a scene***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemList)
* [**GetGroupSceneItemList *Basically GetSceneItemList, but for groups***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetGroupSceneItemList)
* [**GetSceneItemId *Searches a scene for a source, and returns its id***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemId)
* [**CreateSceneItem *Creates a new scene item using a source***](/Broadcasters/OBS/Requests/Scene-Item-Requests/CreateSceneItem)
* [**RemoveSceneItem *Removes a scene item from a scene***](/Broadcasters/OBS/Requests/Scene-Item-Requests/RemoveSceneItem)
* [**DuplicateSceneItem *Duplicates a scene item, copying all transform and crop info***](/Broadcasters/OBS/Requests/Scene-Item-Requests/DuplicateSceneItem)
* [**GetSceneItemTransform *Gets the transform and crop info of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemTransform)
* [**SetSceneItemTransform *Sets the transform and crop info of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemTransform)
* [**GetSceneItemEnabled *Gets the enable state of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemEnabled)
* [**SetSceneItemEnabled *Sets the enable state of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemEnabled)
* [**GetSceneItemLocked *Gets the lock state of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemLocked)
* [**SetSceneItemLocked *Sets the lock state of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemLocked)
* [**GetSceneItemIndex *Gets the index position of a scene item in a scene***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemIndex)
* [**SetSceneItemIndex *Sets the index position of a scene item in a scene***](/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemIndex)
* [**GetSceneItemBlendMode *Gets the blend mode of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/GetSceneItemBlendMode)
* [**SetSceneItemBlendMode *Sets the blend mode of a scene item***](/Broadcasters/OBS/Requests/Scene-Item-Requests/SetSceneItemBlendMode)
{.btn-grid .my-5}

## Output Requests
Output related OBS Studio requests{.subtitle}
* [**GetVirtualCamStatus *Gets the status of the virtualcam output***](/Broadcasters/OBS/Requests/Output-Requests/GetVirtualCamStatus)
* [**ToggleVirtualCam *Toggles the state of the virtualcam output***](/Broadcasters/OBS/Requests/Output-Requests/ToggleVirtualCam)
* [**StartVirtualCam *Starts the virtualcam output***](/Broadcasters/OBS/Requests/Output-Requests/StartVirtualCam)
* [**StopVirtualCam *Stops the virtualcam output***](/Broadcasters/OBS/Requests/Output-Requests/StopVirtualCam)
* [**GetReplayBufferStatus *Gets the status of the replay buffer output***](/Broadcasters/OBS/Requests/Output-Requests/GetReplayBufferStatus)
* [**ToggleReplayBuffer *Toggles the state of the replay buffer output***](/Broadcasters/OBS/Requests/Output-Requests/ToggleReplayBuffer)
* [**StartReplayBuffer *Starts the replay buffer output***](/Broadcasters/OBS/Requests/Output-Requests/StartReplayBuffer)
* [**StopReplayBuffer *Stops the replay buffer output***](/Broadcasters/OBS/Requests/Output-Requests/StopReplayBuffer)
* [**SaveReplayBuffer *Saves the contents of the replay buffer output***](/Broadcasters/OBS/Requests/Output-Requests/SaveReplayBuffer)
* [**GetLastReplayBufferReplay *Gets the filename of the last replay buffer save file***](/Broadcasters/OBS/Requests/Output-Requests/GetLastReplayBufferReplay)
* [**GetOutputList *Gets the list of available outputs***](/Broadcasters/OBS/Requests/Output-Requests/GetOutputList)
* [**GetOutputStatus *Gets the status of an output***](/Broadcasters/OBS/Requests/Output-Requests/GetOutputStatus)
* [**ToggleOutput *Toggles the status of an output***](/Broadcasters/OBS/Requests/Output-Requests/ToggleOutput)
* [**StartOutput *Starts an output***](/Broadcasters/OBS/Requests/Output-Requests/StartOutput)
* [**StopOutput *Stops an output***](/Broadcasters/OBS/Requests/Output-Requests/StopOutput)
* [**GetOutputSettings *Gets the settings of an output***](/Broadcasters/OBS/Requests/Output-Requests/GetOutputSettings)
* [**SetOutputSettings *Sets the settings of an output***](/Broadcasters/OBS/Requests/Output-Requests/SetOutputSettings)
{.btn-grid .my-5}

## Stream Requests
Stream related OBS Studio requests{.subtitle}
* [**GetStreamStatus *Gets the status of the stream output***](/Broadcasters/OBS/Requests/Stream-Requests/GetStreamStatus)
* [**ToggleStream *Toggles the status of the stream output***](/Broadcasters/OBS/Requests/Stream-Requests/ToggleStream)
* [**StartStream *Starts the stream output***](/Broadcasters/OBS/Requests/Stream-Requests/StartStream)
* [**StopStream *Stops the stream output***](/Broadcasters/OBS/Requests/Stream-Requests/StopStream)
* [**SendStreamCaption *Sends CEA-608 caption text over the stream output***](/Broadcasters/OBS/Requests/Stream-Requests/SendStreamCaption)
{.btn-grid .my-5}

## Record Requests
Record related OBS Studio requests{.subtitle}
* [**GetRecordStatus *Gets the status of the record output***](/Broadcasters/OBS/Requests/Record-Requests/GetRecordStatus)
* [**ToggleRecord *Toggles the status of the record output***](/Broadcasters/OBS/Requests/Record-Requests/ToggleRecord)
* [**StartRecord *Starts the record output***](/Broadcasters/OBS/Requests/Record-Requests/StartRecord)
* [**StopRecord *Stops the record output***](/Broadcasters/OBS/Requests/Record-Requests/StopRecord)
* [**ToggleRecordPause *Toggles pause on the record output***](/Broadcasters/OBS/Requests/Record-Requests/ToggleRecordPause)
* [**PauseRecord *Pauses the record output***](/Broadcasters/OBS/Requests/Record-Requests/PauseRecord)
* [**ResumeRecord *Resumes the record output***](/Broadcasters/OBS/Requests/Record-Requests/ResumeRecord)
{.btn-grid .my-5}

## Media Input Requests
Media Input related OBS Studio requests{.subtitle}
* [**GetMediaInputStatus *Gets the status of a media input***](/Broadcasters/OBS/Requests/Media-Input-Requests/GetMediaInputStatus)
* [**SetMediaInputCursor *Sets the cursor position of a media input***](/Broadcasters/OBS/Requests/Media-Input-Requests/SetMediaInputCursor)
* [**OffsetMediaInputCursor *Offsets the current cursor position of a media input by the specified value***](/Broadcasters/OBS/Requests/Media-Input-Requests/OffsetMediaInputCursor)
* [**TriggerMediaInputAction *Triggers an action on a media input***](/Broadcasters/OBS/Requests/Media-Input-Requests/TriggerMediaInputAction)
{.btn-grid .my-5}

## Ui Requests
Ui related OBS Studio requests{.subtitle}
* [**GetStudioModeEnabled *Gets whether studio is enabled***](/Broadcasters/OBS/Requests/Ui-Requests/GetStudioModeEnabled)
* [**SetStudioModeEnabled *Enables or disables studio mode***](/Broadcasters/OBS/Requests/Ui-Requests/SetStudioModeEnabled)
* [**OpenInputPropertiesDialog *Opens the properties dialog of an input***](/Broadcasters/OBS/Requests/Ui-Requests/OpenInputPropertiesDialog)
* [**OpenInputFiltersDialog *Opens the filters dialog of an input***](/Broadcasters/OBS/Requests/Ui-Requests/OpenInputFiltersDialog)
* [**OpenInputInteractDialog *Opens the interact dialog of an input***](/Broadcasters/OBS/Requests/Ui-Requests/OpenInputInteractDialog)
* [**GetMonitorList *Gets a list of connected monitors and information about them***](/Broadcasters/OBS/Requests/Ui-Requests/GetMonitorList)
* [**OpenVideoMixProjector *Opens a projector for a specific output video mix***](/Broadcasters/OBS/Requests/Ui-Requests/OpenVideoMixProjector)
* [**OpenSourceProjector *Opens a projector for a source***](/Broadcasters/OBS/Requests/Ui-Requests/OpenSourceProjector)
{.btn-grid .my-5}

## Additional Request Info
This are examples for requests that existed in privious version of the obs websocket{.subtitle}
* [**RefreshBrowserSource *Refresh a browser source***](/Broadcasters/OBS/Requests/Additional-Request-Info/RefreshBrowserSource)
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/Broadcasters/OBS)
{.btn-grid .my-5}