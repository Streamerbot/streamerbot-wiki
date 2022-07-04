---
title: Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: true
date: 2022-07-03T21:08:27.141Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:46:20.098Z
---

# OBS Events

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## [Scenes](/en/Broadcasters/OBS/Events/Scenes)
* [SwitchScenes](/en/Broadcasters/OBS/Events/Scenes/SwitchScenes)
* [ScenesChanged](/en/Broadcasters/OBS/Events/Scenes/ScenesChanged)
* [SceneCollectionChanged](/en/Broadcasters/OBS/Events/Scenes/SceneCollectionChanged)
* [SceneCollectionListChanged](/en/Broadcasters/OBS/Events/Scenes/SceneCollectionListChanged)
{.links-list}
## [Transitions](/en/Broadcasters/OBS/Events/Transitions)
* [SwitchTransition](/en/Broadcasters/OBS/Events/Transitions/SwitchTransition)
* [TransitionListChanged](/en/Broadcasters/OBS/Events/Transitions/TransitionListChanged)
* [TransitionDurationChanged](/en/Broadcasters/OBS/Events/Transitions/TransitionDurationChanged)
* [TransitionBegin](/en/Broadcasters/OBS/Events/Transitions/TransitionBegin)
* [TransitionEnd](/en/Broadcasters/OBS/Events/Transitions/TransitionEnd)
* [TransitionVideoEnd](/en/Broadcasters/OBS/Events/Transitions/TransitionVideoEnd)
{.links-list}
## [Profiles](/en/Broadcasters/OBS/Events/Profiles)
* [ProfileChanged](/en/Broadcasters/OBS/Events/Profiles/ProfileChanged)
* [ProfileListChanged](/en/Broadcasters/OBS/Events/Profiles/ProfileListChanged)
{.links-list}
## [Streaming](/en/Broadcasters/OBS/Events/Streaming)
* [StreamStarting](/en/Broadcasters/OBS/Events/Streaming/StreamStarting)
* [StreamStarted](/en/Broadcasters/OBS/Events/Streaming/StreamStarted)
* [StreamStopping](/en/Broadcasters/OBS/Events/Streaming/StreamStopping)
* [StreamStopped](/en/Broadcasters/OBS/Events/Streaming/StreamStopped)
* [StreamStatus](/en/Broadcasters/OBS/Events/Streaming/StreamStatus)
{.links-list}
## [Recording](/en/Broadcasters/OBS/Events/Recording)
* [RecordingStarting](/en/Broadcasters/OBS/Events/Recording/RecordingStarting)
* [RecordingStarted](/en/Broadcasters/OBS/Events/Recording/RecordingStarted)
* [RecordingStopping](/en/Broadcasters/OBS/Events/Recording/RecordingStopping)
* [RecordingStopped](/en/Broadcasters/OBS/Events/Recording/RecordingStopped)
* [RecordingPaused](/en/Broadcasters/OBS/Events/Recording/RecordingPaused)
* [RecordingResumed](/en/Broadcasters/OBS/Events/Recording/RecordingResumed)
{.links-list}
## [Virtual Cam](/en/Broadcasters/OBS/Events/Virtual-Cam)
* [VirtualCamStarted](/en/Broadcasters/OBS/Events/Virtual-Cam/VirtualCamStarted)
* [VirtualCamStopped](/en/Broadcasters/OBS/Events/Virtual-Cam/VirtualCamStopped)
{.links-list}
## [Replay Buffer](/en/Broadcasters/OBS/Events/Replay-Buffer)
* [ReplayStarting](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStarting)
* [ReplayStarted](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStarted)
* [ReplayStopping](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStopping)
* [ReplayStopped](/en/Broadcasters/OBS/Events/Replay-Buffer/ReplayStopped)
{.links-list}
## [Other](/en/Broadcasters/OBS/Events/Other)
* [Exiting](/en/Broadcasters/OBS/Events/Other/Exiting)
{.links-list}
## [General](/en/Broadcasters/OBS/Events/General)
* [Heartbeat](/en/Broadcasters/OBS/Events/General/Heartbeat)
* [BroadcastCustomMessage](/en/Broadcasters/OBS/Events/General/BroadcastCustomMessage)
{.links-list}
## [Sources](/en/Broadcasters/OBS/Events/Sources)
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
{.links-list}
## [Media](/en/Broadcasters/OBS/Events/Media)
* [MediaPlaying](/en/Broadcasters/OBS/Events/Media/MediaPlaying)
* [MediaPaused](/en/Broadcasters/OBS/Events/Media/MediaPaused)
* [MediaRestarted](/en/Broadcasters/OBS/Events/Media/MediaRestarted)
* [MediaStopped](/en/Broadcasters/OBS/Events/Media/MediaStopped)
* [MediaNext](/en/Broadcasters/OBS/Events/Media/MediaNext)
* [MediaPrevious](/en/Broadcasters/OBS/Events/Media/MediaPrevious)
* [MediaStarted](/en/Broadcasters/OBS/Events/Media/MediaStarted)
* [MediaEnded](/en/Broadcasters/OBS/Events/Media/MediaEnded)
{.links-list}
## [Scene Items](/en/Broadcasters/OBS/Events/Scene-Items)
* [SourceOrderChanged](/en/Broadcasters/OBS/Events/Scene-Items/SourceOrderChanged)
* [SceneItemAdded](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemAdded)
* [SceneItemRemoved](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemRemoved)
* [SceneItemVisibilityChanged](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemVisibilityChanged)
* [SceneItemLockChanged](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemLockChanged)
* [SceneItemTransformChanged](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemTransformChanged)
* [SceneItemSelected](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemSelected)
* [SceneItemDeselected](/en/Broadcasters/OBS/Events/Scene-Items/SceneItemDeselected)
{.links-list}
## [Studio Mode](/en/Broadcasters/OBS/Events/Studio-Mode)
* [PreviewSceneChanged](/en/Broadcasters/OBS/Events/Studio-Mode/PreviewSceneChanged)
* [StudioModeSwitched](/en/Broadcasters/OBS/Events/Studio-Mode/StudioModeSwitched)
{.links-list}
