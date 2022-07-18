---
title: OBS Studio Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: false
date: 2022-07-18T18:54:05.924Z
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
* [**ExitStarted *OBS has begun the shutdown process***](){.disabled}
* [**VendorEvent *An event has been emitted from a vendor***](){.disabled}
{.btn-grid .my-5}

## Config Events
* [**CurrentSceneCollectionChanging *The current scene collection has begun changing***](){.disabled}
* [**CurrentSceneCollectionChanged *The current scene collection has changed***](){.disabled}
* [**SceneCollectionListChanged *The scene collection list has changed***](){.disabled}
* [**CurrentProfileChanging *The current profile has begun changing***](){.disabled}
* [**CurrentProfileChanged *The current profile has changed***](){.disabled}
* [**ProfileListChanged *The profile list has changed***](){.disabled}
{.btn-grid .my-5}

## Scenes Events
* [**SceneCreated *A new scene has been created***](){.disabled}
* [**SceneRemoved *A scene has been removed***](){.disabled}
* [**SceneNameChanged *The name of a scene has changed***](){.disabled}
* [**CurrentProgramSceneChanged *The current program scene has changed***](){.disabled}
* [**CurrentPreviewSceneChanged *The current preview scene has changed***](){.disabled}
* [**SceneListChanged *The list of scenes has changed***](){.disabled}
{.btn-grid .my-5}

## Inputs Events
* [**InputCreated *An input has been created***](){.disabled}
* [**InputRemoved *An input has been removed***](){.disabled}
* [**InputNameChanged *The name of an input has changed***](){.disabled}
* [**InputActiveStateChanged *An input's active state has changed***](){.disabled}
* [**InputShowStateChanged *An input's show state has changed***](){.disabled}
* [**InputMuteStateChanged *An input's mute state has changed***](){.disabled}
* [**InputVolumeChanged *An input's volume level has changed***](){.disabled}
* [**InputAudioBalanceChanged *The audio balance value of an input has changed***](){.disabled}
* [**InputAudioSyncOffsetChanged *The sync offset of an input has changed***](){.disabled}
* [**InputAudioTracksChanged *The audio tracks of an input have changed***](){.disabled}
* [**InputAudioMonitorTypeChanged *The monitor type of an input has changed***](){.disabled}
* [**InputVolumeMeters *A high-volume event providing volume levels of all active inputs every 50 milliseconds***](){.disabled}
{.btn-grid .my-5}

## Transitions Events
* [**CurrentSceneTransitionChanged *The current scene transition has changed***](){.disabled}
* [**CurrentSceneTransitionDurationChanged *The current scene transition duration has changed***](){.disabled}
{.btn-grid .my-5}
#####
* [**SceneTransitionStarted *A scene transition has started***](){.disabled}
* [**SceneTransitionEnded *A scene transition has completed fully***](){.disabled}
* [**SceneTransitionVideoEnded *A scene transition's video has completed fully***](){.disabled}
{.btn-grid .my-5}

## Filters Events
* [**SourceFilterListReindexed *A source's filter list has been reindexed***](){.disabled}
* [**SourceFilterCreated *A filter has been added to a source***](){.disabled}
* [**SourceFilterRemoved *A filter has been removed from a source***](){.disabled}
* [**SourceFilterNameChanged *The name of a source filter has changed***](){.disabled}
* [**SourceFilterEnableStateChanged *A source filter's enable state has changed***](){.disabled}
{.btn-grid .my-5}

## Scene Items Events
* [**SceneItemCreated *A scene item has been created***](){.disabled}
* [**SceneItemRemoved *A scene item has been removed***](){.disabled}
* [**SceneItemListReindexed *A scene's item list has been reindexed***](){.disabled}
* [**SceneItemEnableStateChanged *A scene item's enable state has changed***](){.disabled}
* [**SceneItemLockStateChanged *A scene item's lock state has changed***](){.disabled}
* [**SceneItemSelected *A scene item has been selected in the Ui***](){.disabled}
* [**SceneItemTransformChanged *The transform/crop of a scene item has changed***](){.disabled}
{.btn-grid .my-5}

## Outputs Events
* [**StreamStateChanged *The state of the stream output has changed***](){.disabled}
* [**RecordStateChanged *The state of the record output has changed***](){.disabled}
* [**ReplayBufferStateChanged *The state of the replay buffer output has changed***](){.disabled}
* [**VirtualcamStateChanged *The state of the virtualcam output has changed***](){.disabled}
* [**ReplayBufferSaved *The replay buffer has been saved***](){.disabled}
{.btn-grid .my-5}

## Media Inputs Events
* [**MediaInputPlaybackStarted *A media input has started playing***](){.disabled}
* [**MediaInputPlaybackEnded *A media input has finished playing***](){.disabled}
* [**MediaInputActionTriggered *An action has been performed on an input***](){.disabled}
{.btn-grid .my-5}

## Ui Events
* [**StudioModeStateChanged *Studio mode has been enabled or disabled***](){.disabled}
{.btn-grid .my-5}

---
- [<i class="mdi mdi-share"></i> **Share your examples! *If you have example(s) for these events you can submit it in #unearthed-arcana on the streamer.bot discord, there is a high change it will come on these pages***](https://discord.gg/RCcH54hWck)
{.btn-grid}
#
- [<i class="mdi mdi-chevron-left"></i>**Events *Go Back***](/en/Events)
- [<img src="https://streamer.bot/img/integrations/obs.svg"/> **OBS Studio *Configure broadcaster: OBS Studio***](/en/Broadcasters/OBS)
{.btn-grid}