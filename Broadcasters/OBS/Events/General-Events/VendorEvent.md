---
title: VendorEvent
description: OBS Studio Events Reference (v5)
published: true
date: 2022-10-29T22:13:21.628Z
tags: 
editor: markdown
dateCreated: 2022-08-07T10:15:10.463Z
---

## Overview
An event has been emitted from a vendor.

A vendor is a unique name registered by a third-party plugin or script, which allows for custom requests and events to be added to obs-websocket. If a plugin or script implements vendor requests or events, documentation is expected to be provided with them.

## Variables
Name | Type | Description | 
----:|:----:|:------------|
`obsEvent.vendorName` | `String`{.datatype} | Name of the vendor emitting the event
`obsEvent.eventType` | `String`{.datatype} | Vendor-provided event typedef
`obsEvent.eventData` | `Object`{.datatype} | Vendor-provided event data. {} if event does not provide any data

## Data Fields
:---|:---:|
| Complexity Rating: | <span class="stars stars--1"></span>
| Latest Supported RPC Version: | *1*{.obs-version-badge}
| Added in | *v5.0.0*{.obs-version-badge}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Events Reference *Go Back***](/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#vendorevent)
{.btn-grid my-5}