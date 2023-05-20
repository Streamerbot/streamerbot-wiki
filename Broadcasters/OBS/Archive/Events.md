---
title: OBS Studio Events (Archive)
description: Reference of all configurable events from OBS Studio (obs-websocket-4.9.1)
published: true
date: 2022-10-29T22:22:12.424Z
tags: obs, obs-studio, events, reference, obs-websocket-4.9.1
editor: markdown
dateCreated: 2022-07-04T19:18:02.800Z
---

![OBS Studio Logo](https://streamer.bot/img/integrations/obs.svg){.align-abstopright}

> **ARCHIVE OF OBS-WEBSOCKET-4.x.x DOCS**
> It is recommended to update to `obs-websocket-5.x.x` and use the latest [OBS Events Docs](/Broadcasters/OBS/Events)
{.is-danger}

This is a full reference of all [OBS WebSocket](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md) events that can be mapped to [actions](/Actions) in Streamer.bot.

> **NOTE**
Some events, such as `SwitchScenes` & `ScenesChanged`, may act as pre & post events.
It is important to consider your use case when deciding which event is best suited for you.
{.is-info}

## General
General & miscellaneous OBS Studio events{.subtitle}
* [**Heartbeat *OBS status update every 2 seconds***](/Broadcasters/OBS/Archive/Events/Heartbeat)
* [**BroadcastCustomMessage *A custom message sent by the OBS server***](/Broadcasters/OBS/Archive/Events/BroadcastCustomMessage)
* [**Exiting *OBS is exiting***](/Broadcasters/OBS/Archive/Events/Exiting)
* [**PreviewSceneChanged *The selected preview scene has changed in Studio Mode***](/Broadcasters/OBS/Archive/Events/Studio-Mode/PreviewSceneChanged)
* [**StudioModeSwitched *Studio Mode has been enabled or disabled***](/Broadcasters/OBS/Archive/Events/Studio-Mode/StudioModeSwitched)
* [**ProfileChanged *Triggered when switching to another profile or when renaming the current profile***](/Broadcasters/OBS/Archive/Events/Profiles/ProfileChanged)
* [**ProfileListChanged *Triggered when a profile is created, added, renamed, or removed***](/Broadcasters/OBS/Archive/Events/Profiles/ProfileListChanged)
{.btn-grid .list .dense .my-5}

## Stream
Events related to current streaming status{.subtitle}
* [**StreamStarting *A request to start streaming has been issued***](/Broadcasters/OBS/Archive/Events/Streaming/StreamStarting)
* [**StreamStarted *Streaming started successfully***](/Broadcasters/OBS/Archive/Events/Streaming/StreamStarted)
* [**StreamStopping *A request to stop streaming has been issued***](/Broadcasters/OBS/Archive/Events/Streaming/StreamStopping)
* [**StreamStopped *Streaming stopped successfully***](/Broadcasters/OBS/Archive/Events/Streaming/StreamStopped)
* [**StreamStatus *Emitted every 2 seconds when stream is active***](/Broadcasters/OBS/Archive/Events/Streaming/StreamStatus)
{.btn-grid .list .dense .my-5}

## Recording
Events related to current recording status{.subtitle}
* [**RecordingStarting *A request to start recording has been issued***](/Broadcasters/OBS/Archive/Events/Recording/RecordingStarting)
* [**RecordingStarted *Recording started successfully***](/Broadcasters/OBS/Archive/Events/Recording/RecordingStarted)
* [**RecordingStopping *A request to stop recording has been issued***](/Broadcasters/OBS/Archive/Events/Recording/RecordingStopping)
* [**RecordingStopped *Recording stopped successfully***](/Broadcasters/OBS/Archive/Events/Recording/RecordingStopped)
* [**RecordingPaused *Current recording paused***](/Broadcasters/OBS/Archive/Events/Recording/RecordingPaused)
* [**RecordingResumed *Current recording resumed***](/Broadcasters/OBS/Archive/Events/Recording/RecordingResumed)
{.btn-grid .list .dense .my-5}

## Scene
Scene change & collection events{.subtitle}
* [**SwitchScenes *Event triggered **before** a scene change***](/Broadcasters/OBS/Archive/Events/Scenes/SwitchScenes)
* [**ScenesChanged *Event triggered **after** a scene change***](/Broadcasters/OBS/Archive/Events/Scenes/ScenesChanged)
* [**SceneCollectionChanged *Triggered when switching to another scene collection***](/Broadcasters/OBS/Archive/Events/Scenes/SceneCollectionChanged)
* [**SceneCollectionListChanged *Triggered when modifying scene collections***](/Broadcasters/OBS/Archive/Events/Scenes/SceneCollectionListChanged)
{.btn-grid .list .dense .my-5}

## Scene Item
Events related to scene item & ordering changes{.subtitle}
* [**SceneItemAdded *A scene item has been added to a scene***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemAdded)
* [**SceneItemRemoved *A scene item has been removed from a scene***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemRemoved)
* [**SceneItemVisibilityChanged *A scene item's visibility has been toggled***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemVisibilityChanged)
* [**SceneItemLockChanged *A scene item's locked status has been toggled***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemLockChanged)
* [**SceneItemTransformChanged *A scene item's transform has been changed***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemTransformChanged)
* [**SceneItemSelected *A scene item is selected***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemSelected)
* [**SceneItemDeselected *A scene item is deselected***](/Broadcasters/OBS/Archive/Events/Scene-Items/SceneItemDeselected)
* [**SourceOrderChanged *Scene items within a scene have been reordered***](/Broadcasters/OBS/Archive/Events/Scene-Items/SourceOrderChanged)
{.btn-grid .list .dense .my-5}

## Transition
Events related to transition changes{.subtitle}
* [**SwitchTransition *The active transition has been changed***](/Broadcasters/OBS/Archive/Events/Transitions/SwitchTransition)
* [**TransitionListChanged *The list of available transitions has been modified. Transitions have been added, removed, or renamed***](/Broadcasters/OBS/Archive/Events/Transitions/TransitionListChanged)
* [**TransitionDurationChanged *The active transition duration has been changed***](/Broadcasters/OBS/Archive/Events/Transitions/TransitionDurationChanged)
* [**TransitionBegin *A transition (other than "cut") has begun***](/Broadcasters/OBS/Archive/Events/Transitions/TransitionBegin)
* [**TransitionEnd *A transition (other than "cut") has ended***](/Broadcasters/OBS/Archive/Events/Transitions/TransitionEnd)
* [**TransitionVideoEnd *A stinger transition has finished playing its video***](/Broadcasters/OBS/Archive/Events/Transitions/TransitionVideoEnd)
{.btn-grid .list .dense .my-5}

## Source
Events related to source & filter changes{.subtitle}
* [**SourceCreated *A source has been created***](/Broadcasters/OBS/Archive/Events/Sources/SourceCreated)
* [**SourceDestroyed *A source has been removed***](/Broadcasters/OBS/Archive/Events/Sources/SourceDestroyed)
* [**SourceVolumeChanged *The volume of a source has changed.***](/Broadcasters/OBS/Archive/Events/Sources/SourceVolumeChanged)
* [**SourceMuteStateChanged *A source has been muted or unmuted***](/Broadcasters/OBS/Archive/Events/Sources/SourceMuteStateChanged)
* [**SourceAudioDeactivated *A source has removed audio***](/Broadcasters/OBS/Archive/Events/Sources/SourceAudioDeactivated)
* [**SourceAudioActivated *A source has added audio***](/Broadcasters/OBS/Archive/Events/Sources/SourceAudioActivated)
* [**SourceAudioSyncOffsetChanged *The audio sync offset of a source has changed***](/Broadcasters/OBS/Archive/Events/Sources/SourceAudioSyncOffsetChanged)
* [**SourceAudioMixersChanged *Audio mixer routing changed on a source***](/Broadcasters/OBS/Archive/Events/Sources/SourceAudioMixersChanged)
* [**SourceRenamed *A source has been renamed***](/Broadcasters/OBS/Archive/Events/Sources/SourceRenamed)
* [**SourceFilterAdded *A filter was added to a source***](/Broadcasters/OBS/Archive/Events/Sources/SourceFilterAdded)
* [**SourceFilterRemoved *A filter was removed from a source***](/Broadcasters/OBS/Archive/Events/Sources/SourceFilterRemoved)
* [**SourceFilterVisibilityChanged *The visibility/enabled state of a filter changed***](/Broadcasters/OBS/Archive/Events/Sources/SourceFilterVisibilityChanged)
* [**SourceFiltersReordered *Filters in a source have been reordered***](/Broadcasters/OBS/Archive/Events/Sources/SourceFiltersReordered)
{.btn-grid .list .dense .my-5}

## Media
Added in obs-websocket *v4.9.0*{.obs-version-badge} {.subtitle}

**Note**: These events are only emitted when something actively controls the media/VLC source. In other words, the source will never emit this on its own naturally.{.subtitle}
* [MediaPlaying](/Broadcasters/OBS/Archive/Events/Media/MediaPlaying)
* [MediaPaused](/Broadcasters/OBS/Archive/Events/Media/MediaPaused)
* [MediaRestarted](/Broadcasters/OBS/Archive/Events/Media/MediaRestarted)
* [MediaStopped](/Broadcasters/OBS/Archive/Events/Media/MediaStopped)
* [MediaNext](/Broadcasters/OBS/Archive/Events/Media/MediaNext)
* [MediaPrevious](/Broadcasters/OBS/Archive/Events/Media/MediaPrevious)
* [MediaStarted](/Broadcasters/OBS/Archive/Events/Media/MediaStarted)
* [MediaEnded](/Broadcasters/OBS/Archive/Events/Media/MediaEnded)
{.btn-grid .list .dense .my-5}

## Replay Buffer
Added in obs-websocket *v4.2.0*{.obs-version-badge} {.subtitle}
* [**ReplayStarting *A request to start the replay buffer has been issued***](/Broadcasters/OBS/Archive/Events/Replay-Buffer/ReplayStarting)
* [**ReplayStarted *Replay Buffer started successfully***](/Broadcasters/OBS/Archive/Events/Replay-Buffer/ReplayStarted)
* [**ReplayStopping *A request to stop the replay buffer has been issued***](/Broadcasters/OBS/Archive/Events/Replay-Buffer/ReplayStopping)
* [**ReplayStopped *Replay Buffer stopped successfully***](/Broadcasters/OBS/Archive/Events/Replay-Buffer/ReplayStopped)
{.btn-grid .list .dense .my-5}

## Virtual Cam
Added in obs-websocket *v4.9.1*{.obs-version-badge} {.subtitle}
* [**VirtualCamStarted *Virtual cam started successfully***](/Broadcasters/OBS/Archive/Events/Virtual-Cam/VirtualCamStarted)
* [**VirtualCamStopped *Virtual cam stopped successfully***](/Broadcasters/OBS/Archive/Events/Virtual-Cam/VirtualCamStopped)
{.btn-grid .list .dense .my-5}

---

* [<i class="mdi mdi-creation primary--text"></i> **Events Reference *Reference of all events in Streamer.bot***](/Events)
* [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/Broadcasters/OBS)
{.btn-grid .my-5}