---
title: (private) OBS Studio Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: false
date: 2022-08-08T11:07:23.982Z
tags: obs, obs-studio, events
editor: markdown
dateCreated: 2022-07-04T19:18:02.800Z
---

> All these events won't exist yet, because streamer.bot is currently on OBS WebSocket *v4.x.x*{.obs-version-badge} 
{.is-danger}

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## Default Variables

Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.event` | *string*{.datatype} | The OBS event's name
`obsEvent.update-type` | *string*{.datatype} | The update type of the OBS event
`obsEvent._json` | *string*{.datatype} | All the variables in a JSON Object

## General Events
General & miscellaneous OBS Studio events{.subtitle}
* [**ExitStarted *OBS has begun the shutdown process***](/en/Broadcasters/OBS/Events/General-Events/ExitStarted)
* [**VendorEvent *An event has been emitted from a vendor***](/en/Broadcasters/OBS/Events/General-Events/VendorEvent)
{.btn-grid .my-5}

## Config Events
Events related to config changes{.subtitle}
* [**CurrentSceneCollectionChanging *The current scene collection has begun changing***](/en/Broadcasters/OBS/Events/Config-Events/CurrentSceneCollectionChanging)
* [**CurrentSceneCollectionChanged *The current scene collection has changed***](/en/Broadcasters/OBS/Events/Config-Events/CurrentSceneCollectionChanged)
* [**SceneCollectionListChanged *The scene collection list has changed***](/en/Broadcasters/OBS/Events/Config-Events/SceneCollectionListChanged)
* [**CurrentProfileChanging *The current profile has begun changing***](/en/Broadcasters/OBS/Events/Config-Events/CurrentProfileChanging)
* [**CurrentProfileChanged *The current profile has changed***](/en/Broadcasters/OBS/Events/Config-Events/CurrentProfileChanged)
* [**ProfileListChanged *The profile list has changed***](/en/Broadcasters/OBS/Events/Config-Events/ProfileListChanged)
{.btn-grid .my-5}

## Scene Events
Events related to scene changes{.subtitle}
* [**SceneCreated *A new scene has been created***](/en/Broadcasters/OBS/Events/Scene-Events/SceneCreated)
* [**SceneRemoved *A scene has been removed***](/en/Broadcasters/OBS/Events/Scene-Events/SceneRemoved)
* [**SceneNameChanged *The name of a scene has changed***](/en/Broadcasters/OBS/Events/Scene-Events/SceneNameChanged)
* [**CurrentProgramSceneChanged *The current program scene has changed***](/en/Broadcasters/OBS/Events/Scene-Events/CurrentProgramSceneChanged)
* [**CurrentPreviewSceneChanged *The current preview scene has changed***](/en/Broadcasters/OBS/Events/Scene-Events/CurrentPreviewSceneChanged)
* [**SceneListChanged *The list of scenes has changed***](/en/Broadcasters/OBS/Events/Scene-Events/SceneListChanged)
{.btn-grid .my-5}

## Input Events
Events related to input changes{.subtitle}
* [**InputCreated *An input has been created***](/en/Broadcasters/OBS/Events/Input-Events/InputCreated)
* [**InputRemoved *An input has been removed***](/en/Broadcasters/OBS/Events/Input-Events/InputRemoved)
* [**InputNameChanged *The name of an input has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputNameChanged)
* [**InputActiveStateChanged *An input's active state has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputActiveStateChanged)
* [**InputShowStateChanged *An input's show state has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputShowStateChanged)
* [**InputMuteStateChanged *An input's mute state has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputMuteStateChanged)
* [**InputVolumeChanged *An input's volume level has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputVolumeChanged)
* [**InputAudioBalanceChanged *The audio balance value of an input has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputAudioBalanceChanged)
* [**InputAudioSyncOffsetChanged *The sync offset of an input has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputAudioSyncOffsetChanged)
* [**InputAudioTracksChanged *The audio tracks of an input have changed***](/en/Broadcasters/OBS/Events/Input-Events/InputAudioTracksChanged)
* [**InputAudioMonitorTypeChanged *The monitor type of an input has changed***](/en/Broadcasters/OBS/Events/Input-Events/InputAudioMonitorTypeChanged)
* [**InputVolumeMeters *A high-volume event providing volume levels of all active inputs every 50 milliseconds***](/en/Broadcasters/OBS/Events/Input-Events/InputVolumeMeters)
{.btn-grid .my-5}

## Transition Events
Events related to transition changes{.subtitle}
* [**CurrentSceneTransitionChanged *The current scene transition has changed***](/en/Broadcasters/OBS/Events/Transition-Events/CurrentSceneTransitionChanged){.disabled}
* [**CurrentSceneTransitionDurationChanged *The current scene transition duration has changed***](/en/Broadcasters/OBS/Events/Transition-Events/CurrentSceneTransitionDurationChanged){.disabled}
{.btn-grid .my-5}
######
* [**SceneTransitionStarted *A scene transition has started***](/en/Broadcasters/OBS/Events/Transition-Events/SceneTransitionStarted){.disabled}
* [**SceneTransitionEnded *A scene transition has completed fully***](/en/Broadcasters/OBS/Events/Transition-Events/SceneTransitionEnded){.disabled}
* [**SceneTransitionVideoEnded *A scene transition's video has completed fully***](/en/Broadcasters/OBS/Events/Transition-Events/SceneTransitionVideoEnded){.disabled}
{.btn-grid .my-5}

## Filter Events
Events related to filter changes{.subtitle}
* [**SourceFilterListReindexed *A source's filter list has been reindexed***](/en/Broadcasters/OBS/Events/Filter-Events/SourceFilterListReindexed){.disabled}
* [**SourceFilterCreated *A filter has been added to a source***](/en/Broadcasters/OBS/Events/Filter-Events/SourceFilterCreated){.disabled}
* [**SourceFilterRemoved *A filter has been removed from a source***](/en/Broadcasters/OBS/Events/Filter-Events/SourceFilterRemoved){.disabled}
* [**SourceFilterNameChanged *The name of a source filter has changed***](/en/Broadcasters/OBS/Events/Filter-Events/SourceFilterNameChanged){.disabled}
* [**SourceFilterEnableStateChanged *A source filter's enable state has changed***](/en/Broadcasters/OBS/Events/Filter-Events/SourceFilterEnableStateChanged){.disabled}
{.btn-grid .my-5}

## Scene Item Events
Events related to scene item changes{.subtitle}
* [**SceneItemCreated *A scene item has been created***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemCreated){.disabled}
* [**SceneItemRemoved *A scene item has been removed***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemRemoved){.disabled}
* [**SceneItemListReindexed *A scene's item list has been reindexed***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemListReindexed){.disabled}
* [**SceneItemEnableStateChanged *A scene item's enable state has changed***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemEnableStateChanged){.disabled}
* [**SceneItemLockStateChanged *A scene item's lock state has changed***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemLockStateChanged){.disabled}
* [**SceneItemSelected *A scene item has been selected in the Ui***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemSelected){.disabled}
* [**SceneItemTransformChanged *The transform/crop of a scene item has changed***](/en/Broadcasters/OBS/Events/Scene-Item-Events/SceneItemTransformChanged){.disabled}
{.btn-grid .my-5}

## Output Events
Events related to current output status{.subtitle}
* [**StreamStateChanged *The state of the stream output has changed***](/en/Broadcasters/OBS/Events/Output-Events/StreamStateChanged){.disabled}
* [**RecordStateChanged *The state of the record output has changed***](/en/Broadcasters/OBS/Events/Output-Events/RecordStateChanged){.disabled}
* [**ReplayBufferStateChanged *The state of the replay buffer output has changed***](/en/Broadcasters/OBS/Events/Output-Events/ReplayBufferStateChanged){.disabled}
* [**VirtualcamStateChanged *The state of the virtualcam output has changed***](/en/Broadcasters/OBS/Events/Output-Events/VirtualcamStateChanged){.disabled}
* [**ReplayBufferSaved *The replay buffer has been saved***](/en/Broadcasters/OBS/Events/Output-Events/ReplayBufferSaved){.disabled}
{.btn-grid .my-5}

## Media Input Events
Events related to media input changes{.subtitle}

**Note**: These events are only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.{.subtitle}

* [**MediaInputPlaybackStarted *A media input has started playing***](/en/Broadcasters/OBS/Events/Media-Input-Events/MediaInputPlaybackStarted){.disabled}
* [**MediaInputPlaybackEnded *A media input has finished playing***](/en/Broadcasters/OBS/Events/Media-Input-Events/MediaInputPlaybackEnded){.disabled}
* [**MediaInputActionTriggered *An action has been performed on an input***](/en/Broadcasters/OBS/Events/Media-Input-Events/MediaInputActionTriggered){.disabled}
{.btn-grid .my-5}

## Ui Events
Events related to Ui changes{.subtitle}
* [**StudioModeStateChanged *Studio mode has been enabled or disabled***](/en/Broadcasters/OBS/Events/Ui-Events/StudioModeStateChanged){.disabled}
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/en/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid .my-5}