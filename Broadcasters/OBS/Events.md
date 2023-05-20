---
title: OBS Studio Events v5
description: Reference of all configurable events from OBS Studio (v5)
published: true
date: 2023-01-10T05:27:58.548Z
tags: obs, obs-studio, events, obs-websocket
editor: markdown
dateCreated: 2022-06-27T02:46:20.098Z
---

 ![OBS Studio Logo](https://streamer.bot/img/integrations/obs.svg){.align-abstopright}
  
 This is a full reference of all [OBS WebSocket 5](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md) events that can be mapped to [actions](/Actions) in Streamer.bot.
 
> Streamer.bot now supports OBS Studio v28 and OBS WebSocket 5.x.
> OBS WebSocket 4.x event documentation can be found [here](/Broadcasters/OBS/Archive/Events)
{.is-info}


## Default Variables
These variables are available on all OBS Studio events{.subtitle}

Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.event` | *string*{.datatype} | The OBS event's name
`obsEvent.update-type` | *string*{.datatype} | The update type of the OBS event
`obsEvent._json` | *string*{.datatype} | All the variables in a JSON Object

## General Events
General OBS Studio events{.subtitle}
* [**ExitStarted *OBS has begun the shutdown process***](/Broadcasters/OBS/Events/General-Events/ExitStarted)
* [**VendorEvent *An event has been emitted from a vendor***](/Broadcasters/OBS/Events/General-Events/VendorEvent)
{.btn-grid .list .dense .my-5}

## Config Events
Events related to config changes{.subtitle}
* [**CurrentSceneCollectionChanging *The current scene collection has begun changing***](/Broadcasters/OBS/Events/Config-Events/CurrentSceneCollectionChanging)
* [**CurrentSceneCollectionChanged *The current scene collection has changed***](/Broadcasters/OBS/Events/Config-Events/CurrentSceneCollectionChanged)
* [**SceneCollectionListChanged *The scene collection list has changed***](/Broadcasters/OBS/Events/Config-Events/SceneCollectionListChanged)
* [**CurrentProfileChanging *The current profile has begun changing***](/Broadcasters/OBS/Events/Config-Events/CurrentProfileChanging)
* [**CurrentProfileChanged *The current profile has changed***](/Broadcasters/OBS/Events/Config-Events/CurrentProfileChanged)
* [**ProfileListChanged *The profile list has changed***](/Broadcasters/OBS/Events/Config-Events/ProfileListChanged)
{.btn-grid .list .dense .my-5}

## Scene Events
Events related to scene changes{.subtitle}
* [**SceneCreated *A new scene has been created***](/Broadcasters/OBS/Events/Scene-Events/SceneCreated)
* [**SceneRemoved *A scene has been removed***](/Broadcasters/OBS/Events/Scene-Events/SceneRemoved)
* [**SceneNameChanged *The name of a scene has changed***](/Broadcasters/OBS/Events/Scene-Events/SceneNameChanged)
* [**CurrentProgramSceneChanged *The current program scene has changed***](/Broadcasters/OBS/Events/Scene-Events/CurrentProgramSceneChanged)
* [**CurrentPreviewSceneChanged *The current preview scene has changed***](/Broadcasters/OBS/Events/Scene-Events/CurrentPreviewSceneChanged)
* [**SceneListChanged *The list of scenes has changed***](/Broadcasters/OBS/Events/Scene-Events/SceneListChanged)
{.btn-grid .list .dense .my-5}

## Input Events
Events related to input changes{.subtitle}
* [**InputCreated *An input has been created***](/Broadcasters/OBS/Events/Input-Events/InputCreated)
* [**InputRemoved *An input has been removed***](/Broadcasters/OBS/Events/Input-Events/InputRemoved)
* [**InputNameChanged *The name of an input has changed***](/Broadcasters/OBS/Events/Input-Events/InputNameChanged)
* [**InputActiveStateChanged *An input's active state has changed***](/Broadcasters/OBS/Events/Input-Events/InputActiveStateChanged)
* [**InputShowStateChanged *An input's show state has changed***](/Broadcasters/OBS/Events/Input-Events/InputShowStateChanged)
* [**InputMuteStateChanged *An input's mute state has changed***](/Broadcasters/OBS/Events/Input-Events/InputMuteStateChanged)
* [**InputVolumeChanged *An input's volume level has changed***](/Broadcasters/OBS/Events/Input-Events/InputVolumeChanged)
* [**InputAudioBalanceChanged *The audio balance value of an input has changed***](/Broadcasters/OBS/Events/Input-Events/InputAudioBalanceChanged)
* [**InputAudioSyncOffsetChanged *The sync offset of an input has changed***](/Broadcasters/OBS/Events/Input-Events/InputAudioSyncOffsetChanged)
* [**InputAudioTracksChanged *The audio tracks of an input have changed***](/Broadcasters/OBS/Events/Input-Events/InputAudioTracksChanged)
* [**InputAudioMonitorTypeChanged *The monitor type of an input has changed***](/Broadcasters/OBS/Events/Input-Events/InputAudioMonitorTypeChanged)
* [**InputVolumeMeters *A high-volume event providing volume levels of all active inputs every 50 milliseconds***](/Broadcasters/OBS/Events/Input-Events/InputVolumeMeters)
{.btn-grid .list .dense .my-5}

## Transition Events
Events related to transition changes{.subtitle}
* [**CurrentSceneTransitionChanged *The current scene transition has changed***](/Broadcasters/OBS/Events/Transition-Events/CurrentSceneTransitionChanged)
* [**CurrentSceneTransitionDurationChanged *The current scene transition duration has changed***](/Broadcasters/OBS/Events/Transition-Events/CurrentSceneTransitionDurationChanged)
* [**SceneTransitionStarted *A scene transition has started***](/Broadcasters/OBS/Events/Transition-Events/SceneTransitionStarted)
* [**SceneTransitionEnded *A scene transition has completed fully***](/Broadcasters/OBS/Events/Transition-Events/SceneTransitionEnded)
* [**SceneTransitionVideoEnded *A scene transition's video has completed fully***](/Broadcasters/OBS/Events/Transition-Events/SceneTransitionVideoEnded)
{.btn-grid .list .dense .my-5}

## Filter Events
Events related to filter changes{.subtitle}
* [**SourceFilterListReindexed *A source's filter list has been reindexed***](/Broadcasters/OBS/Events/Filter-Events/SourceFilterListReindexed)
* [**SourceFilterCreated *A filter has been added to a source***](/Broadcasters/OBS/Events/Filter-Events/SourceFilterCreated)
* [**SourceFilterRemoved *A filter has been removed from a source***](/Broadcasters/OBS/Events/Filter-Events/SourceFilterRemoved)
* [**SourceFilterNameChanged *The name of a source filter has changed***](/Broadcasters/OBS/Events/Filter-Events/SourceFilterNameChanged)
* [**SourceFilterEnableStateChanged *A source filter's enable state has changed***](/Broadcasters/OBS/Events/Filter-Events/SourceFilterEnableStateChanged)
{.btn-grid .list .dense .my-5}

## Scene Item Events
Events related to scene item changes{.subtitle}
* [**SceneItemCreated *A scene item has been created***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemCreated)
* [**SceneItemRemoved *A scene item has been removed***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemRemoved)
* [**SceneItemListReindexed *A scene's item list has been reindexed***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemListReindexed)
* [**SceneItemEnableStateChanged *A scene item's enable state has changed***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemEnableStateChanged)
* [**SceneItemLockStateChanged *A scene item's lock state has changed***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemLockStateChanged)
* [**SceneItemSelected *A scene item has been selected in the Ui***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemSelected)
* [**SceneItemTransformChanged *The transform/crop of a scene item has changed***](/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemTransformChanged)
{.btn-grid .list .dense .my-5}

## Output Events
Events related to current output status{.subtitle}
* [**StreamStateChanged *The state of the stream output has changed***](/Broadcasters/OBS/Events/Output-Events/StreamStateChanged)
* [**RecordStateChanged *The state of the record output has changed***](/Broadcasters/OBS/Events/Output-Events/RecordStateChanged)
* [**ReplayBufferStateChanged *The state of the replay buffer output has changed***](/Broadcasters/OBS/Events/Output-Events/ReplayBufferStateChanged)
* [**VirtualcamStateChanged *The state of the virtualcam output has changed***](/Broadcasters/OBS/Events/Output-Events/VirtualcamStateChanged)
* [**ReplayBufferSaved *The replay buffer has been saved***](/Broadcasters/OBS/Events/Output-Events/ReplayBufferSaved)
{.btn-grid .list .dense .my-5}

## Media Input Events
Events related to media input changes{.subtitle}

**Note**: These events are only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.{.subtitle}

* [**MediaInputPlaybackStarted *A media input has started playing***](/Broadcasters/OBS/Events/Media-Input-Events/MediaInputPlaybackStarted)
* [**MediaInputPlaybackEnded *A media input has finished playing***](/Broadcasters/OBS/Events/Media-Input-Events/MediaInputPlaybackEnded)
* [**MediaInputActionTriggered *An action has been performed on an input***](/Broadcasters/OBS/Events/Media-Input-Events/MediaInputActionTriggered)
{.btn-grid .list .dense .my-5}

## UI Events
Events related to Ui changes{.subtitle}
* [**StudioModeStateChanged *Studio mode has been enabled or disabled***](/Broadcasters/OBS/Events/Ui-Events/StudioModeStateChanged)
* [**ScreenshotSaved *A screenshot has been saved***](/Broadcasters/OBS/Events/Ui-Events/ScreenshotSaved)
{.btn-grid .list .dense .my-5}

## Additional Event Info
Events that are regularly used{.subtitle}
* [**Stream Start/Stop Event *The stream has started or stopped***](/Broadcasters/OBS/Events/Output-Events/StreamStateChanged)
* [**OBS Scene Changed Event *The current program scene has changed***](/Broadcasters/OBS/Events/Scene-Events/CurrentProgramSceneChanged)
{.btn-grid .list .dense .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/Broadcasters/OBS)
{.btn-grid .my-5}