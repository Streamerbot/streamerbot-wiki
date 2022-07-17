---
title: OBS Studio Events
description: Information on OBS events that Streamer.bot can react to using actions.
published: false
date: 2022-07-17T11:50:19.952Z
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
* [**ExitStarted *DESCRIPTION***]()
* [**VendorEvent *DESCRIPTION***]()
{.btn-grid .my-5}

## Config Events
* [**CurrentSceneCollectionChanging *DESCRIPTION***]()
* [**CurrentSceneCollectionChanged *DESCRIPTION***]()
* [**SceneCollectionListChanged *DESCRIPTION***]()
* [**CurrentProfileChanging *DESCRIPTION***]()
* [**CurrentProfileChanged *DESCRIPTION***]()
* [**ProfileListChanged *DESCRIPTION***]()
{.btn-grid .my-5}

## Scenes Events
* [**SceneCreated *DESCRIPTION***]()
* [**SceneRemoved *DESCRIPTION***]()
* [**SceneNameChanged *DESCRIPTION***]()
* [**CurrentProgramSceneChanged *DESCRIPTION***]()
* [**CurrentPreviewSceneChanged *DESCRIPTION***]()
* [**SceneListChanged *DESCRIPTION***]()
{.btn-grid .my-5}

## Inputs Events
* [**InputCreated *DESCRIPTION***]()
* [**InputRemoved *DESCRIPTION***]()
* [**InputNameChanged *DESCRIPTION***]()
* [**InputActiveStateChanged *DESCRIPTION***]()
* [**InputShowStateChanged *DESCRIPTION***]()
* [**InputMuteStateChanged *DESCRIPTION***]()
* [**InputVolumeChanged *DESCRIPTION***]()
* [**InputAudioBalanceChanged *DESCRIPTION***]()
* [**InputAudioSyncOffsetChanged *DESCRIPTION***]()
* [**InputAudioTracksChanged *DESCRIPTION***]()
* [**InputAudioMonitorTypeChanged *DESCRIPTION***]()
* [**InputVolumeMeters *DESCRIPTION***]()
{.btn-grid .my-5}

## Transitions Events
* [**CurrentSceneTransitionChanged *DESCRIPTION***]()
* [**CurrentSceneTransitionDurationChanged *DESCRIPTION***]()
* [**SceneTransitionStarted *DESCRIPTION***]()
* [**SceneTransitionEnded *DESCRIPTION***]()
* [**SceneTransitionVideoEnded *DESCRIPTION***]()
{.btn-grid .my-5}

## Filters Events
* [**SourceFilterListReindexed *DESCRIPTION***]()
* [**SourceFilterCreated *DESCRIPTION***]()
* [**SourceFilterRemoved *DESCRIPTION***]()
* [**SourceFilterNameChanged *DESCRIPTION***]()
* [**SourceFilterEnableStateChanged *DESCRIPTION***]()
{.btn-grid .my-5}

## Scene Items Events
* [**SceneItemCreated *DESCRIPTION***]()
* [**SceneItemRemoved *DESCRIPTION***]()
* [**SceneItemListReindexed *DESCRIPTION***]()
* [**SceneItemEnableStateChanged *DESCRIPTION***]()
* [**SceneItemLockStateChanged *DESCRIPTION***]()
* [**SceneItemSelected *DESCRIPTION***]()
* [**SceneItemTransformChanged *DESCRIPTION***]()
{.btn-grid .my-5}

## Outputs Events
* [**StreamStateChanged *DESCRIPTION***]()
* [**RecordStateChanged *DESCRIPTION***]()
* [**ReplayBufferStateChanged *DESCRIPTION***]()
* [**VirtualcamStateChanged *DESCRIPTION***]()
* [**ReplayBufferSaved *DESCRIPTION***]()
{.btn-grid .my-5}

## Media Inputs Events
* [**MediaInputPlaybackStarted *DESCRIPTION***]()
* [**MediaInputPlaybackEnded *DESCRIPTION***]()
* [**MediaInputActionTriggered *DESCRIPTION***]()
{.btn-grid .my-5}

## Ui Events
* [**StudioModeStateChanged *DESCRIPTION***]()
{.btn-grid .my-5}