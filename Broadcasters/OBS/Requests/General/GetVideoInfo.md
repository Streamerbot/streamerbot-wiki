---
title: GetVideoInfo
description: Get basic OBS video information
published: true
date: 2022-07-04T18:53:08.708Z
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
| `obsRaw.baseHeight` | *integer*{.datatype} | Base (canvas) height
| `obsRaw.baseWidth` | *integer*{.datatype} | Base (canvas) width
| `obsRaw.colorRange` | *string*{.datatype} | Color range (full or partial)
| `obsRaw.colorSpace` | *string*{.datatype} | Color space for YUV
| `obsRaw.fps` | *double*{.datatype} | Frames rendered per second
| `obsRaw.outputHeight` | *integer*{.datatype} | Output height
| `obsRaw.outputWidth` | *integer*{.datatype} | Output width
| `obsRaw.scaleType` | *string*{.datatype} | Scaling method used if output size differs from base size
| `obsRaw.status` | *string*{.datatype} | The status of the OBS raw sub-action
| `obsRaw.videoFormat` | *string*{.datatype} | Video color format
| `obsEvent._json` | *string*{.datatype} | Everything above in a json format

## Explaination
> Details coming soon...
{.is-info}

## Import

```
TlM0RR+LCAAAAAAABACNUj1PwzAQ3ZH4D1YmkDBK0jRp2cpA6YQEiIV0cJxLieTYwY5pq6r/HTtp1HwUCQ+Jfffefby7w/UVQs4PSJUL7jwg/642cFKAeTkvj29Iki3CaAkcJGHoZgnVR56CWPFM3DoNnNDK0JVhfNo3QofmZ1x5auNQfxZOZxOKKQ08HARJhJMk8jAl08zzg1nqgd/EqknfGrTNzzVjZytwkjCw8SqpoWPfUaZTeJKieM5VJeTeQDLCVAfTNtStvpNwI4UuLzbcARG2JXv1qvk4vCQ8FcWilmHspYJTLSXwauwbSdeT7x+115BSQpbvhoqdStta8iGWMY8dCUZbVeFqX0Js7HEvauxY1HEQXILSrFLvYiE3aqh+2yCHupFVPW73dPCFT3sGSZo9IRBAmAVzPE+iBAe+G+E59TPsJyFNk3BCoul0QNxCvvmywrr3bt9jezT2IOyb21mPpfpjwZr6eApWYPdsPbbX9XCcS5uinum6uwWMkVJB2vE2zjpQg2xWv0M1tKIw29Xij7/ZOmHDsgMAAA==
```