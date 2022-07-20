---
title: OpenProjector
description: Open a projector window or create a projector on a monitor. Requires OBS v24.0.4 or newer.
published: true
date: 2022-07-03T21:05:41.896Z
tags: 
editor: markdown
dateCreated: 2022-06-30T15:01:04.324Z
---

# OpenProjector

## Example
```json
{
  "request-type": "OpenProjector",
  "type": "Preview",
  "monitor": "1"
}
```

## Request Fields
| Name | Type | Description |
|-----:|:----:|:------------|
| `type` | *string (Optional)*{.datatype} | Type of projector: `Preview` (default), `Source`, `Scene`, `StudioProgram`, or `Multiview` (case insensitive)
| `monitor` | *int (Optional)*{.datatype} | Monitor to open the projector on. If -1 or omitted, opens a window
| `geometry` | *String (Optional)*{.datatype} | Size and position of the projector window (only if monitor is -1). Encoded in Base64 using Qt's geometry encoding. Corresponds to OBS's saved projectors
| `name` | *String (Optional)*{.datatype} | Name of the source or scene to be displayed (ignored for other projector types)

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
| `obsRaw.status` | *string*{.datatype} | The status of the OBS raw sub-action
| `obsEvent._json` | *string*{.datatype} | Everything above in a json format

## Explaination
> Details coming soon...
{.is-info}

## Import

```
TlM0RR+LCAAAAAAABACNU01vnDAQvVfKf7A4pVJcOSxkUW/JIWlPidreSg5ePGypjE3HOGS12v9efyxZFlKpPgB+7814ZvzYX3wgJHkBNI1WyWeSXgVA8RbcLnm8+06QD4SSB1CAXJLLxw7UE+rfUPUaPyZRz6vexRsX8tPvCdnHl6Ma4RPVOUBeZ2ta59U1zfJ0RYuCFZTlXHC22nCWspgrBP2xYH0Bykp5QkHxjQSfr0cLE/y1klbAPer2S2NcWTsnqbk0E81bR9PyJyduUdvu3ZYnIi4HvjPfrFrmR66Ebm/DHJZspVVlEUH1S24xu7P5/U/xQdMh1M3rfGbH2gYfvS+xVGWC4KZretrvOigdXp6nLZOrqDvxTwgvDQxvTKtVE5SevD7Ch1k9CMbK3vzQt7g18ysbh6IgNP81eIQdF33nMa7ZIdFclcgLxkVBs3XKaLbJBC2gcF5jqxuxEqnI1vPAAZrtL38Z7BM7Z3zbDs9uzuHRH8vp/sOVsT4lwN8JO6GH8fN5boEHf0TwwfPUOVLyzoCYsJEMiaIy/i+TUBfWts6Ro/7wFxU/dbXoAwAA
```