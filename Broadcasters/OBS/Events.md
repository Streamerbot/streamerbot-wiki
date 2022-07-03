---
title: Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: true
date: 2022-07-01T18:12:31.729Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:46:20.098Z
---

# OBS Events

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## [Scenes](/en/Sub-Actions/OBS/Events/Scenes)
* [SwitchScenes](/en/Sub-Actions/OBS/Events/Scenes/SwitchScenes)
* [ScenesChanged](/en/Sub-Actions/OBS/Events/Scenes/ScenesChanged)
* [SceneCollectionChanged](/en/Sub-Actions/OBS/Events/Scenes/SceneCollectionChanged)
* [SceneCollectionListChanged](/en/Sub-Actions/OBS/Events/Scenes/SceneCollectionListChanged)
{.links-list}
## [Transitions](/en/Sub-Actions/OBS/Events/Transitions)
* [SwitchTransition](/en/Sub-Actions/OBS/Events/Transitions/SwitchTransition)
* [TransitionListChanged](/en/Sub-Actions/OBS/Events/Transitions/TransitionListChanged)
* [TransitionDurationChanged](/en/Sub-Actions/OBS/Events/Transitions/TransitionDurationChanged)
* [TransitionBegin](/en/Sub-Actions/OBS/Events/Transitions/TransitionBegin)
* [TransitionEnd](/en/Sub-Actions/OBS/Events/Transitions/TransitionEnd)
* [TransitionVideoEnd](/en/Sub-Actions/OBS/Events/Transitions/TransitionVideoEnd)
{.links-list}
## [Profiles](/en/Sub-Actions/OBS/Events/Profiles)
* [ProfileChanged](/en/Sub-Actions/OBS/Events/Profiles/ProfileChanged)
* [ProfileListChanged](/en/Sub-Actions/OBS/Events/Profiles/ProfileListChanged)
{.links-list}
## [Streaming](/en/Sub-Actions/OBS/Events/Streaming)
* [StreamStarting](/en/Sub-Actions/OBS/Events/Streaming/StreamStarting)
* [StreamStarted](/en/Sub-Actions/OBS/Events/Streaming/StreamStarted)
* [StreamStopping](/en/Sub-Actions/OBS/Events/Streaming/StreamStopping)
* [StreamStopped](/en/Sub-Actions/OBS/Events/Streaming/StreamStopped)
* [StreamStatus](/en/Sub-Actions/OBS/Events/Streaming/StreamStatus)
{.links-list}
## [Recording](/en/Sub-Actions/OBS/Events/Recording)
* [RecordingStarting](/en/Sub-Actions/OBS/Events/Recording/RecordingStarting)
* [RecordingStarted](/en/Sub-Actions/OBS/Events/Recording/RecordingStarted)
* [RecordingStopping](/en/Sub-Actions/OBS/Events/Recording/RecordingStopping)
* [RecordingStopped](/en/Sub-Actions/OBS/Events/Recording/RecordingStopped)
* [RecordingPaused](/en/Sub-Actions/OBS/Events/Recording/RecordingPaused)
* [RecordingResumed](/en/Sub-Actions/OBS/Events/Recording/RecordingResumed)
{.links-list}
## [Virtual Cam](/en/Sub-Actions/OBS/Events/Virtual-Cam)
* [VirtualCamStarted](/en/Sub-Actions/OBS/Events/Virtual-Cam/VirtualCamStarted)
* [VirtualCamStopped](/en/Sub-Actions/OBS/Events/Virtual-Cam/VirtualCamStopped)
{.links-list}
## [Replay Buffer](/en/Sub-Actions/OBS/Events/Replay-Buffer)
* [ReplayStarting](/en/Sub-Actions/OBS/Events/Replay-Buffer/ReplayStarting)
* [ReplayStarted](/en/Sub-Actions/OBS/Events/Replay-Buffer/ReplayStarted)
* [ReplayStopping](/en/Sub-Actions/OBS/Events/Replay-Buffer/ReplayStopping)
* [ReplayStopped](/en/Sub-Actions/OBS/Events/Replay-Buffer/ReplayStopped)
{.links-list}
## [Other](/en/Sub-Actions/OBS/Events/Other)
* [Exiting](/en/Sub-Actions/OBS/Events/Other/Exiting)
{.links-list}
## [General](/en/Sub-Actions/OBS/Events/General)
* [Heartbeat](/en/Sub-Actions/OBS/Events/General/Heartbeat)
* [BroadcastCustomMessage](/en/Sub-Actions/OBS/Events/General/BroadcastCustomMessage)
{.links-list}
## [Sources](/en/Sub-Actions/OBS/Events/Sources)
* [SourceCreated](/en/Sub-Actions/OBS/Events/Sources/SourceCreated)
* [SourceDestroyed](/en/Sub-Actions/OBS/Events/Sources/SourceDestroyed)
* [SourceVolumeChanged](/en/Sub-Actions/OBS/Events/Sources/SourceVolumeChanged)
* [SourceMuteStateChanged](/en/Sub-Actions/OBS/Events/Sources/SourceMuteStateChanged)
* [SourceAudioDeactivated](/en/Sub-Actions/OBS/Events/Sources/SourceAudioDeactivated)
* [SourceAudioActivated](/en/Sub-Actions/OBS/Events/Sources/SourceAudioActivated)
* [SourceAudioSyncOffsetChanged](/en/Sub-Actions/OBS/Events/Sources/SourceAudioSyncOffsetChanged)
* [SourceAudioMixersChanged](/en/Sub-Actions/OBS/Events/Sources/SourceAudioMixersChanged)
* [SourceRenamed](/en/Sub-Actions/OBS/Events/Sources/SourceRenamed)
* [SourceFilterAdded](/en/Sub-Actions/OBS/Events/Sources/SourceFilterAdded)
* [SourceFilterRemoved](/en/Sub-Actions/OBS/Events/Sources/SourceFilterRemoved)
* [SourceFilterVisibilityChanged](/en/Sub-Actions/OBS/Events/Sources/SourceFilterVisibilityChanged)
* [SourceFiltersReordered](/en/Sub-Actions/OBS/Events/Sources/SourceFiltersReordered)
{.links-list}
## [Media](/en/Sub-Actions/OBS/Events/Media)
* [MediaPlaying](/en/Sub-Actions/OBS/Events/Media/MediaPlaying)
* [MediaPaused](/en/Sub-Actions/OBS/Events/Media/MediaPaused)
* [MediaRestarted](/en/Sub-Actions/OBS/Events/Media/MediaRestarted)
* [MediaStopped](/en/Sub-Actions/OBS/Events/Media/MediaStopped)
* [MediaNext](/en/Sub-Actions/OBS/Events/Media/MediaNext)
* [MediaPrevious](/en/Sub-Actions/OBS/Events/Media/MediaPrevious)
* [MediaStarted](/en/Sub-Actions/OBS/Events/Media/MediaStarted)
* [MediaEnded](/en/Sub-Actions/OBS/Events/Media/MediaEnded)
{.links-list}
## [Scene Items](/en/Sub-Actions/OBS/Events/Scene-Items)
* [SourceOrderChanged](/en/Sub-Actions/OBS/Events/Scene-Items/SourceOrderChanged)
* [SceneItemAdded](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemAdded)
* [SceneItemRemoved](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemRemoved)
* [SceneItemVisibilityChanged](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemVisibilityChanged)
* [SceneItemLockChanged](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemLockChanged)
* [SceneItemTransformChanged](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemTransformChanged)
* [SceneItemSelected](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemSelected)
* [SceneItemDeselected](/en/Sub-Actions/OBS/Events/Scene-Items/SceneItemDeselected)
{.links-list}
## [Studio Mode](/en/Sub-Actions/OBS/Events/Studio-Mode)
* [PreviewSceneChanged](/en/Sub-Actions/OBS/Events/Studio-Mode/PreviewSceneChanged)
* [StudioModeSwitched](/en/Sub-Actions/OBS/Events/Studio-Mode/StudioModeSwitched)
{.links-list}
