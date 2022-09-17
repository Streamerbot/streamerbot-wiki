---
title: UDP Interface
description: Run TwitchSpeaker stuff trough Streamer.bot
published: true
date: 2022-09-17T16:13:32.697Z
tags: 
editor: markdown
dateCreated: 2022-09-17T15:23:48.991Z
---

Port: `6669`

Payload Data (currently available):
```json
{ "command": "pause" }
{ "command": "resume" }
{ "command": "clear" }
{ "command": "off" }
{ "command": "disable" }
{ "command": "on" }
{ "command": "enable" }
{ "command": "stop" }
{ "command": "events", "value": "", "state": "on" }
{ "command": "events", "value": "", "state": "off" }
{ "command": "reg", "mode": "add", "user": "%user%", "id": "%userId%" }
{ "command": "reg", "mode": "del", "user": "%user%", "id": "%userId%" }
{ "command": "profile", "profile": "none" }
{ "command": "profile", "profile": "<profile name>" 
```
## Examples

<details style="margin: 0.5em 0em;">
<summary>pause</summary>
  
```json
{
  "command": "pause"
}
```
  
</details>

<details style="margin: 0.5em 0em;">
<summary>resume</summary>

```json
{
  "command": "resume"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>clear</summary>

```json
{
  "command": "clear"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>off</summary>
  
```json
{
  "command": "off"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>disable</summary>

```json
{
  "command": "disable"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>on</summary>

```json
{
  "command": "on"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>enable</summary>

```json
{
  "command": "enable"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>stop</summary>

```json
{
  "command": "stop"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>events (on)</summary>

```json
{
  "command": "events",
  "value": "",
  "state": "on"
}
```

**Example:**
```json
{
  "command": "events",
  "value": "<event name>",
  "state": "on"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>events (off)</summary>

```json
{
  "command": "events",
  "value": "",
  "state": "off"
}
```

**Example:**
```json
{
  "command": "events",
  "value": "<event name>",
  "state": "off"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>reg (add)</summary>

```json
{
  "command": "reg",
  "mode": "add",
  "user": "",
  "id": ""
}
```

**Example:**
```json
{
  "command": "reg",
  "mode": "add",
  "user": "%user%",
  "id": "%userId%"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>reg (del)</summary>

```json
{
  "command": "reg",
  "mode": "del",
  "user": "",
  "id": ""
}
```

**Example:**
```json
{
  "command": "reg",
  "mode": "del",
  "user": "%user%",
  "id": "%userId%"
}
```
</details>

<details style="margin: 0.5em 0em;">
<summary>profile</summary>

```json
{
  "command": "profile",
  "profile": ""
}
```

**Example:**
```json
{
  "command": "profile",
  "profile": "<profile name>"
}
```

</details>

<details style="margin: 0.5em 0em;">
<summary>profile (none)</summary>

```json
{
  "command": "profile", 
  "profile": "none"
}
```

</details>
You can also send text to be spoken

 ```json
{
  "command": "speak",
  "id": "<id>",
  "voice": "<voice alias>",
  "message": "<msg>"
}
```