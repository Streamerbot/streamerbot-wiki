---
title: OBS Studio Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: false
date: 2022-08-07T09:55:39.201Z
tags: obs, obs-studio, events
editor: markdown
dateCreated: 2022-07-04T19:18:02.800Z
---

> All these events won't exist yet, because streamer.bot is currently on OBS websocket *v4.x.x*{.version-badge} 
> Event Title `White` = `Page exist`
> Event Title `Gray` = `Page doesn't exist`
{.is-danger}

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## General Events
General & miscellaneous OBS Studio events{.subtitle}
* [**ExitStarted *OBS has begun the shutdown process***](/en/Broadcasters/OBS/Events/General-Events/ExitStarted){.disabled}
* [**VendorEvent *An event has been emitted from a vendor***](/en/Broadcasters/OBS/Events/General-Events/VendorEvent){.disabled}
{.btn-grid .my-5}

## Config Events
Events related to config changes{.subtitle}
* [**CurrentSceneCollectionChanging *The current scene collection has begun changing***](/en/Broadcasters/OBS/Events/Config-Events/CurrentSceneCollectionChanging){.disabled}
* [**CurrentSceneCollectionChanged *The current scene collection has changed***](/en/Broadcasters/OBS/Events/Config-Events/CurrentSceneCollectionChanged){.disabled}
* [**SceneCollectionListChanged *The scene collection list has changed***](/en/Broadcasters/OBS/Events/Config-Events/SceneCollectionListChanged){.disabled}
* [**CurrentProfileChanging *The current profile has begun changing***](/en/Broadcasters/OBS/Events/Config-Events/CurrentProfileChanging){.disabled}
* [**CurrentProfileChanged *The current profile has changed***](/en/Broadcasters/OBS/Events/Config-Events/CurrentProfileChanged){.disabled}
* [**ProfileListChanged *The profile list has changed***](/en/Broadcasters/OBS/Events/Config-Events/ProfileListChanged){.disabled}
{.btn-grid .my-5}

## Scenes Events
Events related to scene changes{.subtitle}
* [**SceneCreated *A new scene has been created***](/en/Broadcasters/OBS/Events/Scenes-Events/SceneCreated){.disabled}
* [**SceneRemoved *A scene has been removed***](/en/Broadcasters/OBS/Events/Scenes-Events/SceneRemoved){.disabled}
* [**SceneNameChanged *The name of a scene has changed***](/en/Broadcasters/OBS/Events/Scenes-Events/SceneNameChanged){.disabled}
* [**CurrentProgramSceneChanged *The current program scene has changed***](/en/Broadcasters/OBS/Events/Scenes-Events/CurrentProgramSceneChanged){.disabled}
* [**CurrentPreviewSceneChanged *The current preview scene has changed***](/en/Broadcasters/OBS/Events/Scenes-Events/CurrentPreviewSceneChanged){.disabled}
* [**SceneListChanged *The list of scenes has changed***](/en/Broadcasters/OBS/Events/Scenes-Events/SceneListChanged){.disabled}
{.btn-grid .my-5}

## Inputs Events
Events related to input changes{.subtitle}
* [**InputCreated *An input has been created***](/en/Broadcasters/OBS/Events/Inputs-Events/InputCreated){.disabled}
* [**InputRemoved *An input has been removed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputRemoved){.disabled}
* [**InputNameChanged *The name of an input has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputNameChanged){.disabled}
* [**InputActiveStateChanged *An input's active state has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputActiveStateChanged){.disabled}
* [**InputShowStateChanged *An input's show state has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputShowStateChanged){.disabled}
* [**InputMuteStateChanged *An input's mute state has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputMuteStateChanged){.disabled}
* [**InputVolumeChanged *An input's volume level has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputVolumeChanged){.disabled}
* [**InputAudioBalanceChanged *The audio balance value of an input has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputAudioBalanceChanged){.disabled}
* [**InputAudioSyncOffsetChanged *The sync offset of an input has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputAudioSyncOffsetChanged){.disabled}
* [**InputAudioTracksChanged *The audio tracks of an input have changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputAudioTracksChanged){.disabled}
* [**InputAudioMonitorTypeChanged *The monitor type of an input has changed***](/en/Broadcasters/OBS/Events/Inputs-Events/InputAudioMonitorTypeChanged){.disabled}
* [**InputVolumeMeters *A high-volume event providing volume levels of all active inputs every 50 milliseconds***](/en/Broadcasters/OBS/Events/Inputs-Events/InputVolumeMeters){.disabled}
{.btn-grid .my-5}

## Transitions Events
Events related to transition changes{.subtitle}
* [**CurrentSceneTransitionChanged *The current scene transition has changed***](/en/Broadcasters/OBS/Events/Transitions-Events/CurrentSceneTransitionChanged){.disabled}
* [**CurrentSceneTransitionDurationChanged *The current scene transition duration has changed***](/en/Broadcasters/OBS/Events/Transitions-Events/CurrentSceneTransitionDurationChanged){.disabled}
{.btn-grid .my-5}
######
* [**SceneTransitionStarted *A scene transition has started***](/en/Broadcasters/OBS/Events/Transitions-Events/SceneTransitionStarted){.disabled}
* [**SceneTransitionEnded *A scene transition has completed fully***](/en/Broadcasters/OBS/Events/Transitions-Events/SceneTransitionEnded){.disabled}
* [**SceneTransitionVideoEnded *A scene transition's video has completed fully***](/en/Broadcasters/OBS/Events/Transitions-Events/SceneTransitionVideoEnded){.disabled}
{.btn-grid .my-5}

## Filters Events
Events related to filter changes{.subtitle}
* [**SourceFilterListReindexed *A source's filter list has been reindexed***](/en/Broadcasters/OBS/Events/Filters-Events/SourceFilterListReindexed){.disabled}
* [**SourceFilterCreated *A filter has been added to a source***](/en/Broadcasters/OBS/Events/Filters-Events/SourceFilterCreated){.disabled}
* [**SourceFilterRemoved *A filter has been removed from a source***](/en/Broadcasters/OBS/Events/Filters-Events/SourceFilterRemoved){.disabled}
* [**SourceFilterNameChanged *The name of a source filter has changed***](/en/Broadcasters/OBS/Events/Filters-Events/SourceFilterNameChanged){.disabled}
* [**SourceFilterEnableStateChanged *A source filter's enable state has changed***](/en/Broadcasters/OBS/Events/Filters-Events/SourceFilterEnableStateChanged){.disabled}
{.btn-grid .my-5}

## Scene Items Events
Events related to scene item changes{.subtitle}
* [**SceneItemCreated *A scene item has been created***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemCreated){.disabled}
* [**SceneItemRemoved *A scene item has been removed***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemRemoved){.disabled}
* [**SceneItemListReindexed *A scene's item list has been reindexed***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemListReindexed){.disabled}
* [**SceneItemEnableStateChanged *A scene item's enable state has changed***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemEnableStateChanged){.disabled}
* [**SceneItemLockStateChanged *A scene item's lock state has changed***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemLockStateChanged){.disabled}
* [**SceneItemSelected *A scene item has been selected in the Ui***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemSelected){.disabled}
* [**SceneItemTransformChanged *The transform/crop of a scene item has changed***](/en/Broadcasters/OBS/Events/Scene-Items-Events/SceneItemTransformChanged){.disabled}
{.btn-grid .my-5}

## Outputs Events
Events related to current output status{.subtitle}
* [**StreamStateChanged *The state of the stream output has changed***](/en/Broadcasters/OBS/Events/){.disabled}
* [**RecordStateChanged *The state of the record output has changed***](){.disabled}
* [**ReplayBufferStateChanged *The state of the replay buffer output has changed***](){.disabled}
* [**VirtualcamStateChanged *The state of the virtualcam output has changed***](){.disabled}
* [**ReplayBufferSaved *The replay buffer has been saved***](){.disabled}
{.btn-grid .my-5}

## Media Inputs Events
Events related to media input changes{.subtitle}

**Note**: These events are only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.{.subtitle}

* [**MediaInputPlaybackStarted *A media input has started playing***](/en/Broadcasters/OBS/Events/Media-Inputs-Events/MediaInputPlaybackStarted){.disabled}
* [**MediaInputPlaybackEnded *A media input has finished playing***](/en/Broadcasters/OBS/Events/Media-Inputs-Events/MediaInputPlaybackEnded){.disabled}
* [**MediaInputActionTriggered *An action has been performed on an input***](/en/Broadcasters/OBS/Events/Media-Inputs-Events/MediaInputActionTriggered){.disabled}
{.btn-grid .my-5}

## Ui Events
Events related to Ui changes{.subtitle}
* [**StudioModeStateChanged *Studio mode has been enabled or disabled***](/en/Broadcasters/OBS/Events/Ui-Events/StudioModeStateChanged){.disabled}
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/en/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid .my-5}