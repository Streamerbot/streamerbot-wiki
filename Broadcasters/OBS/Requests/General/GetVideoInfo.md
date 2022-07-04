---
title: GetVideoInfo
description: Get basic OBS video information
published: true
date: 2022-07-04T18:53:04.909Z
tags: 
editor: markdown
dateCreated: 2022-06-30T14:50:06.558Z
---

# GetVideoInfo

## Example
```json
{
"request-type": "GetVideoInfo"
}
```

## Request Fields
> No request fields required.
{.is-success}

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
| `obsRaw.baseHeight` | <kbd>integer</kbd> | Base (canvas) height
| `obsRaw.baseWidth` | <kbd>integer</kbd> | Base (canvas) width
| `obsRaw.colorRange` | <kbd>string</kbd> | Color range (full or partial)
| `obsRaw.colorSpace` | <kbd>string</kbd> | Color space for YUV
| `obsRaw.fps` | <kbd>double</kbd> | Frames rendered per second
| `obsRaw.outputHeight` | <kbd>integer</kbd> | Output height
| `obsRaw.outputWidth` | <kbd>integer</kbd> | Output width
| `obsRaw.scaleType` | <kbd>string</kbd> | Scaling method used if output size differs from base size
| `obsRaw.status` | <kbd>string</kbd> | The status of the OBS raw sub-action
| `obsRaw.videoFormat` | <kbd>string</kbd> | Video color format
| `obsEvent._json` | <kbd>string</kbd> | Everything above in a json format

## Explaination
> Details coming soon...
{.is-info}

## Import

```
TlM0RR+LCAAAAAAABACNUj1PwzAQ3ZH4D1YmkDBK0jRp2cpA6YQEiIV0cJxLieTYwY5pq6r/HTtp1HwUCQ+Jfffefby7w/UVQs4PSJUL7jwg/642cFKAeTkvj29Iki3CaAkcJGHoZgnVR56CWPFM3DoNnNDK0JVhfNo3QofmZ1x5auNQfxZOZxOKKQ08HARJhJMk8jAl08zzg1nqgd/EqknfGrTNzzVjZytwkjCw8SqpoWPfUaZTeJKieM5VJeTeQDLCVAfTNtStvpNwI4UuLzbcARG2JXv1qvk4vCQ8FcWilmHspYJTLSXwauwbSdeT7x+115BSQpbvhoqdStta8iGWMY8dCUZbVeFqX0Js7HEvauxY1HEQXILSrFLvYiE3aqh+2yCHupFVPW73dPCFT3sGSZo9IRBAmAVzPE+iBAe+G+E59TPsJyFNk3BCoul0QNxCvvmywrr3bt9jezT2IOyb21mPpfpjwZr6eApWYPdsPbbX9XCcS5uinum6uwWMkVJB2vE2zjpQg2xWv0M1tKIw29Xij7/ZOmHDsgMAAA==
```