---
title: TransitionEnd
description: OBS Studio Events Reference
published: true
date: 2022-07-18T16:11:32.926Z
tags: 
editor: markdown
dateCreated: 2022-06-27T02:42:12.078Z
---

---
title: TransitionEnd
description: A transition (other than "cut") has ended. Note: The `from-scene` field is not available in TransitionEnd.
published: true
date: 2022-07-03T21:48:26.429Z
tags:
editor: markdown
dateCreated: 2022-06-27T02:42:12.078Z
---

# TransitionEnd

## Variables

Name | Description
----:|:------------
| `obsEvent.event` | The OBS event in this case `TransitionEnd`
| `obsEvent.duration` | The duration of the transition
| `obsEvent.name` | The name of the transition
| `obsEvent.to-scene` | On which scene the transition has ended
| `obsEvent.type	` | The type of transition that had began
| `obsEvent.update-type	` | The update type of the OBS event in this case `TransitionEnd`
| `obsEvent._json` | Everything above in a json format
---

- [<i class="mdi mdi-chevron-left"></i>**Back to the OBS events page*Go Back***](/en/Broadcasters/OBS/Events)
- [<i class="mdi mdi-github"></i> **OBS Websocket documentation *This links to the GitHub documentation of this specific event***](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#transitionend)
{.btn-grid my-5}
