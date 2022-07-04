---
title: GetVersion
description: Returns the latest version of the plugin and the API.
published: true
date: 2022-07-03T21:05:24.187Z
tags: 
editor: markdown
dateCreated: 2022-06-27T10:44:13.410Z
---

# GetVersion

## Example
```json
{
"request-type": "GetVersion"
}
```

## Request Fields
> No request fields required.
{.is-success}

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
| `obsEvent.obs-studio-version` | <kbd>string</kbd> |  OBSRemote compatible API version. Fixed to 1.1 for retrocompatibility
| `obsRaw.obs-websocket-version` | <kbd>string</kbd> | obs-websocket plugin version
| `obsRaw.version` | <kbd>double</kbd> | OBSRemote compatible API version. Fixed to 1.1 for retrocompatibility.
| `obsRaw.status` | <kbd>string</kbd> | The status of the OBS raw sub-action
| `obsEvent._json` | <kbd>string</kbd> | Everything above in a json format

## Explaination
> Details coming soon...
{.is-info}

## Import
```
TlM0RR+LCAAAAAAABACFUsFOwzAMvSPxD1FPIBGUdV23chsHBickQFzoDlnijkppWpKGMU37d5Jm1bp2iBzaxH5+tp+9u7xAKPgGpfNSBncovGkMkhZgX8Hz/StSdIMwWoAERQW6WkD97uHXgQdTVtuXtvgP90Zo53/WlXPHsiJTOmFZhinLAEd8FOEkiac4HE+m03gShsBmnqsJ+jJgXHZphDhaQdKVAMdXKwMd+w8ThsODKovHXNel2lpIRoXuYNp2jrV30q1VaaqzzXZAVGzoVr8YOSRXVPKymDciDL2slMwoBbIe+gbCnYj3b+UNoFKQ5T99tQ6FbVzoLlWpTAMFVldd43pbQWrtaYczDRxm36NWoI2o9Vs5V2vd171tTkLTxFMzaHI4+MynPb0kfkNGjJCIJQnOOE1wNIoSnDAW45CQmDO64uNZ0gvcQL7+dKKSW3LqcR1aexSfmts5D4X6Y7V8fZKDk5ccrfv2uuyPcuFSNPNcdjdACFpp4B2vdzZEHumXvhNqw4rCblaL3/8CRaUUP6oDAAA=
```