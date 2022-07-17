---
title: OBS Studio Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: false
date: 2022-07-17T12:01:36.220Z
tags: obs, obs-studio, events
editor: markdown
dateCreated: 2022-07-04T19:18:02.800Z
---

# OBS Events
> You need to have obs websocket *v5.x.x*{.version-badge} installed
{.is-warning}

There are a handful of events that the OBS websocket broadcasts when things occur within OBS itself.

It's important to note, that while it may seem like one event maybe the one to use, there is the possibility that another one is better suited for the use case.

For example, a single scene change, fires off more events then just changing the scene, there are the transition events the happen, a pre and post event for the switch, etc.

## General Events
* [**ExitStarted *OBS has begun the shutdown process***]()
* [**VendorEvent *An event has been emitted from a vendor***]()
{.btn-grid .my-5}

## Config Events
* [**CurrentSceneCollectionChanging *The current scene collection has begun changing***]()
* [**CurrentSceneCollectionChanged *The current scene collection has changed***]()
* [**SceneCollectionListChanged *The scene collection list has changed***]()
* [**CurrentProfileChanging *The current profile has begun changing***]()
* [**CurrentProfileChanged *The current profile has changed***]()
* [**ProfileListChanged *The profile list has changed***]()
{.btn-grid .my-5}

## Scenes Events
* [**SceneCreated *A new scene has been created***]()
* [**SceneRemoved *A scene has been removed***]()
* [**SceneNameChanged *The name of a scene has changed***]()
* [**CurrentProgramSceneChanged *The current program scene has changed***]()
* [**CurrentPreviewSceneChanged *The current preview scene has changed***]()
* [**SceneListChanged *The list of scenes has changed***]()
{.btn-grid .my-5}

## Inputs Events
* [**InputCreated *An input has been created***]()
* [**InputRemoved *An input has been removed***]()
* [**InputNameChanged *The name of an input has changed***]()
* [**InputActiveStateChanged *An input's active state has changed***]()
* [**InputShowStateChanged *An input's show state has changed***]()
* [**InputMuteStateChanged *An input's mute state has changed***]()
* [**InputVolumeChanged *An input's volume level has changed***]()
* [**InputAudioBalanceChanged *The audio balance value of an input has changed***]()
* [**InputAudioSyncOffsetChanged *The sync offset of an input has changed***]()
* [**InputAudioTracksChanged *The audio tracks of an input have changed***]()
* [**InputAudioMonitorTypeChanged *The monitor type of an input has changed***]()
* [**InputVolumeMeters *A high-volume event providing volume levels of all active inputs every 50 milliseconds***]()
{.btn-grid .my-5}

## Transitions Events
* [**CurrentSceneTransitionChanged *The current scene transition has changed***]()
* [**CurrentSceneTransitionDurationChanged *The current scene transition duration has changed***]()
{.btn-grid .my-5}
#####
* [**SceneTransitionStarted *A scene transition has started***]()
* [**SceneTransitionEnded *A scene transition has completed fully***]()
* [**SceneTransitionVideoEnded *A scene transition's video has completed fully***]()
{.btn-grid .my-5}

## Filters Events
* [**SourceFilterListReindexed *A source's filter list has been reindexed***]()
* [**SourceFilterCreated *A filter has been added to a source***]()
* [**SourceFilterRemoved *A filter has been removed from a source***]()
* [**SourceFilterNameChanged *The name of a source filter has changed***]()
* [**SourceFilterEnableStateChanged *A source filter's enable state has changed***]()
{.btn-grid .my-5}

## Scene Items Events
* [**SceneItemCreated *A scene item has been created***]()
* [**SceneItemRemoved *A scene item has been removed***]()
* [**SceneItemListReindexed *A scene's item list has been reindexed***]()
* [**SceneItemEnableStateChanged *A scene item's enable state has changed***]()
* [**SceneItemLockStateChanged *A scene item's lock state has changed***]()
* [**SceneItemSelected *A scene item has been selected in the Ui***]()
* [**SceneItemTransformChanged *The transform/crop of a scene item has changed***]()
{.btn-grid .my-5}

## Outputs Events
* [**StreamStateChanged *The state of the stream output has changed***]()
* [**RecordStateChanged *The state of the record output has changed***]()
* [**ReplayBufferStateChanged *The state of the replay buffer output has changed***]()
* [**VirtualcamStateChanged *The state of the virtualcam output has changed***]()
* [**ReplayBufferSaved *The replay buffer has been saved***]()
{.btn-grid .my-5}

## Media Inputs Events
* [**MediaInputPlaybackStarted *A media input has started playing***]()
* [**MediaInputPlaybackEnded *A media input has finished playing***]()
* [**MediaInputActionTriggered *An action has been performed on an input***]()
{.btn-grid .my-5}

## Ui Events
* [**StudioModeStateChanged *Studio mode has been enabled or disabled***]()
{.btn-grid .my-5}