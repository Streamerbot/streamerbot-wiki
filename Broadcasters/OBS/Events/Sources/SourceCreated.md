---
title: SourceCreated
description: OBS Studio Events Reference
published: true
date: 2022-07-06T20:54:51.214Z
tags:
editor: markdown
dateCreated: 2022-06-28T13:55:54.310Z
---

# SourceCreated

## Variables

| Variable | Description |
|---------:|:------------|
| `obsEvent.event` | The OBS event in this case `SourceCreated`
| `obsEvent.sourceKind` | Source kind
| `obsEvent.sourceName` | Source name
| `obsEvent.sourceSettings.#` | The settings of this source  <span style="color:red">*Change the `#` with the specific setting*</span>
| `obsEvent.sourceType` | Source type <span style="color:blue">Can be `input`, `scene`, `transition` or `filter`.</span>
| `obsEvent.update-type` | The update type of the OBS event in this case `SourceCreated`
| `obsEvent._json` | Everything above in a json format

---

 [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#sourcecreated)
{.btn-grid my-5}
