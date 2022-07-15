---
title: OBS Studio Events
description: Reference of all configurable events from OBS Studio
published: true
date: 2022-07-15T15:23:30.448Z
tags: obs, obs-studio, events, reference
editor: markdown
dateCreated: 2022-06-27T02:46:20.098Z
---

![OBS Studio Logo](https://streamer.bot/img/integrations/obs.svg){.align-abstopright}


This is a full reference of all [OBS WebSocket](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md) events that can be mapped to [actions](/en/Actions) in Streamer.bot.

> **NOTE**
> Some events, such as `SwitchScenes` & `ScenesChanged`, may act as pre & post events. 
> It is important to consider your use case when deciding which event is best suited for you.
{.is-info}

## General
General & miscellaneous OBS Studio events{.subtitle}
* [**Heartbeat *OBS status update every 2 seconds***](/en/Broadcasters/OBS/Events/General/Heartbeat)
* [**BroadcastCustomMessage *A custom message sent by the OBS server***](/en/Broadcasters/OBS/Events/General/BroadcastCustomMessage)
* [**Exiting *OBS is exiting***](/en/Broadcasters/OBS/Events/Other/Exiting)
* [**PreviewSceneChanged *The selected preview scene has changed in Studio Mode***](/en/Broadcasters/OBS/Events/Studio-Mode/PreviewSceneChanged)
* [**StudioModeSwitched *Studio Mode has been enabled or disabled***](/en/Broadcasters/OBS/Events/Studio-Mode/StudioModeSwitched)
* [**ProfileChanged *Triggered when switching to another profile or when renaming the current profile***](/en/Broadcasters/OBS/Events/Profiles/ProfileChanged)
* [**ProfileListChanged *Triggered when a profile is created, added, renamed, or removed***](/en/Broadcasters/OBS/Events/Profiles/ProfileListChanged)
{.btn-grid .my-5}

## Stream
Events related to current streaming status{.subtitle}
* [**StreamStarting *A request to start streaming has been issued***](/en/Broadcasters/OBS/Events/Streaming/StreamStarting)
* [**StreamStarted *Streaming started successfully***](/en/Broadcasters/OBS/Events/Streaming/StreamStarted)
* [**StreamStopping *A request to stop streaming has been issued***](/en/Broadcasters/OBS/Events/Streaming/StreamStopping)
* [**StreamStopped *Streaming stopped successfully***](/en/Broadcasters/OBS/Events/Streaming/StreamStopped)
* [**StreamStatus *Emitted every 2 seconds when stream is active***](/en/Broadcasters/OBS/Events/Streaming/StreamStatus)
{.btn-grid .my-5}

## Recording
Events related to current recording status{.subtitle}
* [**RecordingStarting *A request to start recording has been issued***](/en/Broadcasters/OBS/Events/Recording/RecordingStarting)
* [**RecordingStarted *Recording started successfully***](/en/Broadcasters/OBS/Events/Recording/RecordingStarted)
* [**RecordingStopping *A request to stop recording has been issued***](/en/Broadcasters/OBS/Events/Recording/RecordingStopping)
* [**RecordingStopped *Recording stopped successfully***](/en/Broadcasters/OBS/Events/Recording/RecordingStopped)
* [**RecordingPaused *Current recording paused***](/en/Broadcasters/OBS/Events/Recording/RecordingPaused)
* [**RecordingResumed *Current recording resumed***](/en/Broadcasters/OBS/Events/Recording/RecordingResumed)
{.btn-grid .my-5}

## Scene
Scene change & collection events{.subtitle}
* [**SwitchScenes *Event triggered **before** a scene change***](/en/Broadcasters/OBS/Events/Scenes/SwitchScenes)
* [**ScenesChanged *Event triggered **after** a scene change***](/en/Broadcasters/OBS/Events/Scenes/ScenesChanged)
* [**SceneCollectionChanged *Triggered when switching to another scene collection***](/en/Broadcasters/OBS/Events/Scenes/SceneCollectionChanged)
* [**SceneCollectionListChanged *Triggered when modifying scene collections***](/en/Broadcasters/OBS/Events/Scenes/SceneCollectionListChanged)
{.btn-grid .my-5}

## Scene Item
Events related to scene item & ordering changes{.subtitle}
* [**SceneItemAdded *A scene item has been added to a scene***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemAdded)
* [**SceneItemRemoved *A scene item has been removed from a scene***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemRemoved)
* [**SceneItemVisibilityChanged *A scene item's visibility has been toggled***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemVisibilityChanged)
* [**SceneItemLockChanged *A scene item's locked status has been toggled***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemLockChanged)
* [**SceneItemTransformChanged *A scene item's transform has been changed***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemTransformChanged)
* [**SceneItemSelected *A scene item is selected***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemSelected)
* [**SceneItemDeselected *A scene item is deselected***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemDeselected)
* [**SourceOrderChanged *Scene items within a scene have been reordered***](/en/Broadcasters/OBS/Events/Scene-Items/SourceOrderChanged)
{.btn-grid .my-5}

## Transition
Events related to transition changes{.subtitle}
* [**SwitchTransition *The active transition has been changed***](/en/Broadcasters/OBS/Events/Transitions/SwitchTransition)
* [**TransitionListChanged *The list of available transitions has been modified. Transitions have been added, removed, or renamed***](/en/Broadcasters/OBS/Events/Transitions/TransitionListChanged)
* [**TransitionDurationChanged *The active transition duration has been changed***](/en/Broadcasters/OBS/Events/Transitions/TransitionDurationChanged)
* [**TransitionBegin *A transition (other than "cut") has begun***](/en/Broadcasters/OBS/Events/Transitions/TransitionBegin)
* [**TransitionEnd *A transition (other than "cut") has ended***](/en/Broadcasters/OBS/Events/Transitions/TransitionEnd)
* [**TransitionVideoEnd *A stinger transition has finished playing its video***](/en/Broadcasters/OBS/Events/Transitions/TransitionVideoEnd)
{.btn-grid .my-5}

## Source
Events related to source & filter changes{.subtitle}
* [**SourceCreated *A source has been created***](/en/Broadcasters/OBS/Events/Sources/SourceCreated)
* [**SourceDestroyed *A source has been removed***](/en/Broadcasters/OBS/Events/Sources/SourceDestroyed)
* [**SourceVolumeChanged *The volume of a source has changed.***](/en/Broadcasters/OBS/Events/Sources/SourceVolumeChanged)
* [**SourceMuteStateChanged *A source has been muted or unmuted***](/en/Broadcasters/OBS/Events/Sources/SourceMuteStateChanged)
* [**SourceAudioDeactivated *A source has removed audio***](/en/Broadcasters/OBS/Events/Sources/SourceAudioDeactivated)
* [**SourceAudioActivated *A source has added audio***](/en/Broadcasters/OBS/Events/Sources/SourceAudioActivated)
* [**SourceAudioSyncOffsetChanged *The audio sync offset of a source has changed***](/en/Broadcasters/OBS/Events/Sources/SourceAudioSyncOffsetChanged)
* [**SourceAudioMixersChanged *Audio mixer routing changed on a source***](/en/Broadcasters/OBS/Events/Sources/SourceAudioMixersChanged)
* [**SourceRenamed *A source has been renamed***](/en/Broadcasters/OBS/Events/Sources/SourceRenamed)
* [**SourceFilterAdded *A filter was added to a source***](/en/Broadcasters/OBS/Events/Sources/SourceFilterAdded)
* [**SourceFilterRemoved *A filter was removed from a source***](/en/Broadcasters/OBS/Events/Sources/SourceFilterRemoved)
* [**SourceFilterVisibilityChanged *The visibility/enabled state of a filter changed***](/en/Broadcasters/OBS/Events/Sources/SourceFilterVisibilityChanged)
* [**SourceFiltersReordered *Filters in a source have been reordered***](/en/Broadcasters/OBS/Events/Sources/SourceFiltersReordered)
{.btn-grid .my-5}

## Media
Added in obs-websocket v4.9.0{.subtitle}

**Note**: These events are only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.{.subtitle}
* [MediaPlaying](/en/Broadcasters/OBS/Events/Media/MediaPlaying)
* [MediaPaused](/en/Broadcasters/OBS/Events/Media/MediaPaused)
* [MediaRestarted](/en/Broadcasters/OBS/Events/Media/MediaRestarted)
* [MediaStopped](/en/Broadcasters/OBS/Events/Media/MediaStopped)
* [MediaNext](/en/Broadcasters/OBS/Events/Media/MediaNext)
* [MediaPrevious](/en/Broadcasters/OBS/Events/Media/MediaPrevious)
* [MediaStarted](/en/Broadcasters/OBS/Events/Media/MediaStarted)
* [MediaEnded](/en/Broadcasters/OBS/Events/Media/MediaEnded)
{.btn-grid .my-5}

## Replay Buffer
Added in obs-websocket v4.2.0{.subtitle}
* [**ReplayStarting *A request to start the replay buffer has been issued***](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStarting)
* [**ReplayStarted *Replay Buffer started successfully***](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStarted)
* [**ReplayStopping *A request to stop the replay buffer has been issued***](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStopping)
* [**ReplayStopped *Replay Buffer stopped successfully***](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStopped)
{.btn-grid .my-5}

## Virtual Cam
Added in obs-websocket v4.9.1{.subtitle}
* [**VirtualCamStarted *Virtual cam started successfully***](/en/Broadcasters/OBS/Events/Virtual-Cam/VirtualCamStarted)
* [**VirtualCamStopped *Virtual cam stopped successfully***](/en/Broadcasters/OBS/Events/Virtual-Cam/VirtualCamStopped)
{.btn-grid .my-5}


---{.my-10}

* [<i class="mdi mdi-creation primary--text"></i> **Events Reference *Reference of all events in Streamer.bot***](/en/Events)
* [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid}