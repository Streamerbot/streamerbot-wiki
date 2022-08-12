---
title: CallVendorRequest
description: OBS Studio Requests Reference (v5)
published: false
date: 2022-08-12T11:54:53.598Z
tags: 
editor: markdown
dateCreated: 2022-08-07T08:32:45.548Z
---

## Overview
Call a request registered to a vendor.

A vendor is a unique name registered by a third-party plugin or script, which allows for custom requests and events to be added to obs-websocket. If a plugin or script implements vendor requests or events, documentation is expected to be provided with them.

## Request Fields
Name | Type | Required| Description |
----:|:----:|:-------:|:------------|
`vendorName` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | Name of the vendor to use
`requestType` | `String`{.datatype} | <i class="mdi mdi-check-bold"></i> | The request type to call
`requestData` | `Object`{.datatype} | <i class="mdi mdi-close-thick"></i> | Object containing appropriate request data

## Variables
Name | Type | Description | 
----:|:---------:|:------------|
`obsRaw.vendorName` | `String`{.datatype} | Echoed of `vendorName`
`obsRaw.requestType` | `String`{.datatype} | Echoed of `requestType`
`obsRaw.responseData` | `Object`{.datatype} | Object containing appropriate response data. {} if request does not provide any response data

## Data Fields
:---|:---:|
Complexity Rating: | <span class="stars stars--3"></span>
Latest Supported RPC Version: | *1*{.obs-version-badge}
Added in | *v5.0.0*{.obs-version-badge}

## Usage
## Tabset {.tabset}
### OBS raw
```json

```
## End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i>**OBS Studio Requests Reference *Go Back***](/en/Broadcasters/OBS/Requests)
- [<i class="mdi mdi-github"></i> **OBS WebSocket Documentation *GitHub documentation for this request***](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#callvendorrequest)
{.btn-grid .my-5}