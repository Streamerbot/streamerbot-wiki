---
title: OBS Studio Events
description: Reference of all configurable events from OBS Studio
published: true
date: 2022-07-15T15:03:40.337Z
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
* [**Heartbeat *OBS status update every 2 seconds***](/en/Broadcasters/OBS/Events/General/Heartbeat)
* [**BroadcastCustomMessage *A custom message sent by the OBS server***](/en/Broadcasters/OBS/Events/General/BroadcastCustomMessage)
* [**Exiting *OBS is exiting***](/en/Broadcasters/OBS/Events/Other/Exiting)
* [**PreviewSceneChanged *The selected preview scene has changed in Studio Mode***](/en/Broadcasters/OBS/Events/Studio-Mode/PreviewSceneChanged)
* [**StudioModeSwitched *Studio Mode has been enabled or disabled***](/en/Broadcasters/OBS/Events/Studio-Mode/StudioModeSwitched)
{.btn-grid}

## Stream
* [**StreamStarting *A request to start streaming has been issued***](/en/Broadcasters/OBS/Events/Streaming/StreamStarting)
* [**StreamStarted *Streaming started successfully***](/en/Broadcasters/OBS/Events/Streaming/StreamStarted)
* [**StreamStopping *A request to stop streaming has been issued***](/en/Broadcasters/OBS/Events/Streaming/StreamStopping)
* [**StreamStopped *Streaming stopped successfully***](/en/Broadcasters/OBS/Events/Streaming/StreamStopped)
* [**StreamStatus *Emitted every 2 seconds when stream is active***](/en/Broadcasters/OBS/Events/Streaming/StreamStatus)
{.btn-grid}

## Recording
* [RecordingStarting](/en/Broadcasters/OBS/Events/Recording/RecordingStarting)
* [RecordingStarted](/en/Broadcasters/OBS/Events/Recording/RecordingStarted)
* [RecordingStopping](/en/Broadcasters/OBS/Events/Recording/RecordingStopping)
* [RecordingStopped](/en/Broadcasters/OBS/Events/Recording/RecordingStopped)
* [RecordingPaused](/en/Broadcasters/OBS/Events/Recording/RecordingPaused)
* [RecordingResumed](/en/Broadcasters/OBS/Events/Recording/RecordingResumed)
{.btn-grid}

## Scene
* [**SwitchScenes *Event triggered **before** a scene change***](/en/Broadcasters/OBS/Events/Scenes/SwitchScenes)
* [**ScenesChanged *Event triggered **after** a scene change***](/en/Broadcasters/OBS/Events/Scenes/ScenesChanged)
* [**SceneCollectionChanged *Triggered when switching to another scene collection***](/en/Broadcasters/OBS/Events/Scenes/SceneCollectionChanged)
* [**SceneCollectionListChanged *Triggered when modifying scene collections***](/en/Broadcasters/OBS/Events/Scenes/SceneCollectionListChanged)
{.btn-grid}

## Scene Item
* [**SceneItemAdded *A scene item has been added to a scene***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemAdded)
* [**SceneItemRemoved *A scene item has been removed from a scene***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemRemoved)
* [**SceneItemVisibilityChanged *A scene item's visibility has been toggled***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemVisibilityChanged)
* [**SceneItemLockChanged *A scene item's locked status has been toggled***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemLockChanged)
* [**SceneItemTransformChanged *A scene item's transform has been changed***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemTransformChanged)
* [**SceneItemSelected *A scene item is selected***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemSelected)
* [**SceneItemDeselected *A scene item is deselected***](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemDeselected)
{.btn-grid}

## Transition
* [SwitchTransition](/en/Broadcasters/OBS/Events/Transitions/SwitchTransition)
* [TransitionListChanged](/en/Broadcasters/OBS/Events/Transitions/TransitionListChanged)
* [TransitionDurationChanged](/en/Broadcasters/OBS/Events/Transitions/TransitionDurationChanged)
* [TransitionBegin](/en/Broadcasters/OBS/Events/Transitions/TransitionBegin)
* [TransitionEnd](/en/Broadcasters/OBS/Events/Transitions/TransitionEnd)
* [TransitionVideoEnd](/en/Broadcasters/OBS/Events/Transitions/TransitionVideoEnd)
{.btn-grid}

## Profile
* [ProfileChanged](/en/Broadcasters/OBS/Events/Profiles/ProfileChanged)
* [ProfileListChanged](/en/Broadcasters/OBS/Events/Profiles/ProfileListChanged)
{.btn-grid}

## Virtual Cam
* [VirtualCamStarted](/en/Broadcasters/OBS/Events/Virtual-Cam/VirtualCamStarted)
* [VirtualCamStopped](/en/Broadcasters/OBS/Events/Virtual-Cam/VirtualCamStopped)
{.btn-grid}

## Replay Buffer
* [ReplayStarting](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStarting)
* [ReplayStarted](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStarted)
* [ReplayStopping](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStopping)
* [ReplayStopped](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStopped)
{.btn-grid}

## Source
* [SourceCreated](/en/Broadcasters/OBS/Events/Sources/SourceCreated)
* [SourceDestroyed](/en/Broadcasters/OBS/Events/Sources/SourceDestroyed)
* [SourceVolumeChanged](/en/Broadcasters/OBS/Events/Sources/SourceVolumeChanged)
* [SourceMuteStateChanged](/en/Broadcasters/OBS/Events/Sources/SourceMuteStateChanged)
* [SourceAudioDeactivated](/en/Broadcasters/OBS/Events/Sources/SourceAudioDeactivated)
* [SourceAudioActivated](/en/Broadcasters/OBS/Events/Sources/SourceAudioActivated)
* [SourceAudioSyncOffsetChanged](/en/Broadcasters/OBS/Events/Sources/SourceAudioSyncOffsetChanged)
* [SourceAudioMixersChanged](/en/Broadcasters/OBS/Events/Sources/SourceAudioMixersChanged)
* [SourceRenamed](/en/Broadcasters/OBS/Events/Sources/SourceRenamed)
* [SourceFilterAdded](/en/Broadcasters/OBS/Events/Sources/SourceFilterAdded)
* [SourceFilterRemoved](/en/Broadcasters/OBS/Events/Sources/SourceFilterRemoved)
* [SourceFilterVisibilityChanged](/en/Broadcasters/OBS/Events/Sources/SourceFilterVisibilityChanged)
* [SourceFiltersReordered](/en/Broadcasters/OBS/Events/Sources/SourceFiltersReordered)
* [SourceOrderChanged](/en/Broadcasters/OBS/Events/Scene-Items/SourceOrderChanged)
{.btn-grid}

## Media
* [MediaPlaying](/en/Broadcasters/OBS/Events/Media/MediaPlaying)
* [MediaPaused](/en/Broadcasters/OBS/Events/Media/MediaPaused)
* [MediaRestarted](/en/Broadcasters/OBS/Events/Media/MediaRestarted)
* [MediaStopped](/en/Broadcasters/OBS/Events/Media/MediaStopped)
* [MediaNext](/en/Broadcasters/OBS/Events/Media/MediaNext)
* [MediaPrevious](/en/Broadcasters/OBS/Events/Media/MediaPrevious)
* [MediaStarted](/en/Broadcasters/OBS/Events/Media/MediaStarted)
* [MediaEnded](/en/Broadcasters/OBS/Events/Media/MediaEnded)
{.btn-grid}
