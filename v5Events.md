---
title: Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: true
date: 2022-07-04T19:18:02.800Z
tags: 
editor: markdown
dateCreated: 2022-07-04T19:18:02.800Z
---

# OBS Events

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## General Events
* [ExitStarted]()
* [VendorEvent]()
* [Config Events]()
* [CurrentSceneCollectionChanging]()
* [CurrentSceneCollectionChanged]()
* [SceneCollectionListChanged]()
* [CurrentProfileChanging]()
* [CurrentProfileChanged]()
* [ProfileListChanged]()
{.links-list}
## Scenes Events
* [SceneCreated]()
* [SceneRemoved]()
* [SceneNameChanged]()
* [CurrentProgramSceneChanged]()
* [CurrentPreviewSceneChanged]()
* [SceneListChanged]()
{.links-list}
## Inputs Events
* [InputCreated]()
* [InputRemoved]()
* [InputNameChanged]()
* [InputActiveStateChanged]()
* [InputShowStateChanged]()
* [InputMuteStateChanged]()
* [InputVolumeChanged]()
* [InputAudioBalanceChanged]()
* [InputAudioSyncOffsetChanged]()
* [InputAudioTracksChanged]()
* [InputAudioMonitorTypeChanged]()
* [InputVolumeMeters]()
{.links-list}
## Transitions Events
* [CurrentSceneTransitionChanged]()
* [CurrentSceneTransitionDurationChanged]()
* [SceneTransitionStarted]()
* [SceneTransitionEnded]()
* [SceneTransitionVideoEnded]()
{.links-list}
## Filters Events
* [SourceFilterListReindexed]()
* [SourceFilterCreated]()
* [SourceFilterRemoved]()
* [SourceFilterNameChanged]()
* [SourceFilterEnableStateChanged]()
{.links-list}
## Scene Items Events
* [SceneItemCreated]()
* [SceneItemRemoved]()
* [SceneItemListReindexed]()
* [SceneItemEnableStateChanged]()
* [SceneItemLockStateChanged]()
* [SceneItemSelected]()
* [SceneItemTransformChanged]()
{.links-list}
## Outputs Events
* [StreamStateChanged]()
* [RecordStateChanged]()
* [ReplayBufferStateChanged]()
* [VirtualcamStateChanged]()
* [ReplayBufferSaved]()
{.links-list}
## Media Inputs Events
* [MediaInputPlaybackStarted]()
* [MediaInputPlaybackEnded]()
* [MediaInputActionTriggered]()
{.links-list}
## Ui Events
* [StudioModeStateChanged]()
{.links-list}
