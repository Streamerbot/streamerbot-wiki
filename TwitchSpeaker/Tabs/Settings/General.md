---
title: UDP Interface
description: Run TwitchSpeaker stuff trough Streamer.bot
published: true
date: 2022-09-17T16:08:14.630Z
tags: 
editor: markdown
dateCreated: 2022-09-17T15:23:48.991Z
---

Port: `6669`

Payload Data (currently available):
{.my-5}
<div>
<details>
<summary>pause</summary>
  
```json
{
  "command": "pause"
}
```
  
</details>

<details>
<summary>resume</summary>

```json
{
  "command": "resume"
}
```

</details>

<details>
<summary>clear</summary>

```json
{
  "command": "clear"
}
```

</details>

<details>
<summary>off</summary>
```json
{
  "command": "off"
}
```

</details>

<details>
<summary>disable</summary>

```json
{
  "command": "disable"
}
```

</details>

<details>
<summary>on</summary>

```json
{
  "command": "on"
}
```

</details>

<details>
<summary>enable</summary>
## enable
```json
{
  "command": "enable"
}
```

</details>

<details>
<summary>stop</summary>

```json
{
  "command": "stop"
}
```

</details>

<details>
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

<details>
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

<details>
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

<details>
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

<details>
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

<details>
<summary>profile (none)</summary>

```json
{
  "command": "profile", 
  "profile": "none"
}
```

</details>
</div>
You can also send text to be spoken

 ```json
{
  "command": "speak",
  "id": "<id>",
  "voice": "<voice alias>",
  "message": "<msg>"
}
```