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

## [Scenes](/en/Integrations/OBS/OBS-Events/Scenes)
* [SwitchScenes](/en/Integrations/OBS/OBS-Events/Scenes/SwitchScenes)
* [ScenesChanged](/en/Integrations/OBS/OBS-Events/Scenes/ScenesChanged)
* [SceneCollectionChanged](/en/Integrations/OBS/OBS-Events/Scenes/SceneCollectionChanged)
* [SceneCollectionListChanged](/en/Integrations/OBS/OBS-Events/Scenes/SceneCollectionListChanged)
{.links-list}
## [Transitions](/en/Integrations/OBS/OBS-Events/Transitions)
* [SwitchTransition](/en/Integrations/OBS/OBS-Events/Transitions/SwitchTransition)
* [TransitionListChanged](/en/Integrations/OBS/OBS-Events/Transitions/TransitionListChanged)
* [TransitionDurationChanged](/en/Integrations/OBS/OBS-Events/Transitions/TransitionDurationChanged)
* [TransitionBegin](/en/Integrations/OBS/OBS-Events/Transitions/TransitionBegin)
* [TransitionEnd](/en/Integrations/OBS/OBS-Events/Transitions/TransitionEnd)
* [TransitionVideoEnd](/en/Integrations/OBS/OBS-Events/Transitions/TransitionVideoEnd)
{.links-list}
## [Profiles](/en/Integrations/OBS/OBS-Events/Profiles)
* [ProfileChanged](/en/Integrations/OBS/OBS-Events/Profiles/ProfileChanged)
* [ProfileListChanged](/en/Integrations/OBS/OBS-Events/Profiles/ProfileListChanged)
{.links-list}
## [Streaming](/en/Integrations/OBS/OBS-Events/Streaming)
* [StreamStarting](/en/Integrations/OBS/OBS-Events/Streaming/StreamStarting)
* [StreamStarted](/en/Integrations/OBS/OBS-Events/Streaming/StreamStarted)
* [StreamStopping](/en/Integrations/OBS/OBS-Events/Streaming/StreamStopping)
* [StreamStopped](/en/Integrations/OBS/OBS-Events/Streaming/StreamStopped)
* [StreamStatus](/en/Integrations/OBS/OBS-Events/Streaming/StreamStatus)
{.links-list}
## [Recording](/en/Integrations/OBS/OBS-Events/Recording)
* [RecordingStarting](/en/Integrations/OBS/OBS-Events/Recording/RecordingStarting)
* [RecordingStarted](/en/Integrations/OBS/OBS-Events/Recording/RecordingStarted)
* [RecordingStopping](/en/Integrations/OBS/OBS-Events/Recording/RecordingStopping)
* [RecordingStopped](/en/Integrations/OBS/OBS-Events/Recording/RecordingStopped)
* [RecordingPaused](/en/Integrations/OBS/OBS-Events/Recording/RecordingPaused)
* [RecordingResumed](/en/Integrations/OBS/OBS-Events/Recording/RecordingResumed)
{.links-list}
## [Virtual Cam](/en/Integrations/OBS/OBS-Events/Virtual-Cam)
* [VirtualCamStarted](/en/Integrations/OBS/OBS-Events/Virtual-Cam/VirtualCamStarted)
* [VirtualCamStopped](/en/Integrations/OBS/OBS-Events/Virtual-Cam/VirtualCamStopped)
{.links-list}
## [Replay Buffer](/en/Integrations/OBS/OBS-Events/Replay-Buffer)
* [ReplayStarting](/en/Integrations/OBS/OBS-Events/Replay-Buffer/ReplayStarting)
* [ReplayStarted](/en/Integrations/OBS/OBS-Events/Replay-Buffer/ReplayStarted)
* [ReplayStopping](/en/Integrations/OBS/OBS-Events/Replay-Buffer/ReplayStopping)
* [ReplayStopped](/en/Integrations/OBS/OBS-Events/Replay-Buffer/ReplayStopped)
{.links-list}
## [Other](/en/Integrations/OBS/OBS-Events/Other)
* [Exiting](/en/Integrations/OBS/OBS-Events/Other/Exiting)
{.links-list}
## [General](/en/Integrations/OBS/OBS-Events/General)
* [Heartbeat](/en/Integrations/OBS/OBS-Events/General/Heartbeat)
* [BroadcastCustomMessage](/en/Integrations/OBS/OBS-Events/General/BroadcastCustomMessage)
{.links-list}
## [Sources](/en/Integrations/OBS/OBS-Events/Sources)
* [SourceCreated](/en/Integrations/OBS/OBS-Events/Sources/SourceCreated)
* [SourceDestroyed](/en/Integrations/OBS/OBS-Events/Sources/SourceDestroyed)
* [SourceVolumeChanged](/en/Integrations/OBS/OBS-Events/Sources/SourceVolumeChanged)
* [SourceMuteStateChanged](/en/Integrations/OBS/OBS-Events/Sources/SourceMuteStateChanged)
* [SourceAudioDeactivated](/en/Integrations/OBS/OBS-Events/Sources/SourceAudioDeactivated)
* [SourceAudioActivated](/en/Integrations/OBS/OBS-Events/Sources/SourceAudioActivated)
* [SourceAudioSyncOffsetChanged](/en/Integrations/OBS/OBS-Events/Sources/SourceAudioSyncOffsetChanged)
* [SourceAudioMixersChanged](/en/Integrations/OBS/OBS-Events/Sources/SourceAudioMixersChanged)
* [SourceRenamed](/en/Integrations/OBS/OBS-Events/Sources/SourceRenamed)
* [SourceFilterAdded](/en/Integrations/OBS/OBS-Events/Sources/SourceFilterAdded)
* [SourceFilterRemoved](/en/Integrations/OBS/OBS-Events/Sources/SourceFilterRemoved)
* [SourceFilterVisibilityChanged](/en/Integrations/OBS/OBS-Events/Sources/SourceFilterVisibilityChanged)
* [SourceFiltersReordered](/en/Integrations/OBS/OBS-Events/Sources/SourceFiltersReordered)
{.links-list}
## [Media](/en/Integrations/OBS/OBS-Events/Media)
* [MediaPlaying](/en/Integrations/OBS/OBS-Events/Media/MediaPlaying)
* [MediaPaused](/en/Integrations/OBS/OBS-Events/Media/MediaPaused)
* [MediaRestarted](/en/Integrations/OBS/OBS-Events/Media/MediaRestarted)
* [MediaStopped](/en/Integrations/OBS/OBS-Events/Media/MediaStopped)
* [MediaNext](/en/Integrations/OBS/OBS-Events/Media/MediaNext)
* [MediaPrevious](/en/Integrations/OBS/OBS-Events/Media/MediaPrevious)
* [MediaStarted](/en/Integrations/OBS/OBS-Events/Media/MediaStarted)
* [MediaEnded](/en/Integrations/OBS/OBS-Events/Media/MediaEnded)
{.links-list}
## [Scene Items](/en/Integrations/OBS/OBS-Events/Scene-Items)
* [SourceOrderChanged](/en/Integrations/OBS/OBS-Events/Scene-Items/SourceOrderChanged)
* [SceneItemAdded](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemAdded)
* [SceneItemRemoved](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemRemoved)
* [SceneItemVisibilityChanged](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemVisibilityChanged)
* [SceneItemLockChanged](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemLockChanged)
* [SceneItemTransformChanged](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemTransformChanged)
* [SceneItemSelected](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemSelected)
* [SceneItemDeselected](/en/Integrations/OBS/OBS-Events/Scene-Items/SceneItemDeselected)
{.links-list}
## [Studio Mode](/en/Integrations/OBS/OBS-Events/Studio-Mode)
* [PreviewSceneChanged](/en/Integrations/OBS/OBS-Events/Studio-Mode/PreviewSceneChanged)
* [StudioModeSwitched](/en/Integrations/OBS/OBS-Events/Studio-Mode/StudioModeSwitched)
{.links-list}
