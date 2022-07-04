---
title: Raw
description: OBS raw is powerfull tool to do OBS things that you can't do in regular sub-actions.
published: true
date: 2022-07-03T02:27:50.885Z
tags: obs, raw
editor: markdown
dateCreated: 2021-11-02T04:00:37.158Z
---

# Raw

Since there are quite a large number of possible commands that can be sent to OBS via obs-websocket, its not possible to have every single one, along with all the different options available, as a simple sub-aciton.

OBS Raw, will let you take full control over sending data to OBS.

![sub-action-obs-raw-001.png](/sub-action-obs-raw-001.png)

## Name
For better organization in your sub-action list, give it a name

## variables
To use variables in the JSON request, add the % variable surrounded by quotes, it must still be valid JSON to parse properly.  The variable will be auto-typed when it is parsed to be sent to OBS, so if the variable is a number, the resulting JSON will not have double quotes around the value.

## Return Values
When the OBS Raw is executed, result will be places in the argument stack for the action.

Since the result is returned in JSON, it will walk the entire tree, and add each value as a `obsRaw.<JSON Path>` for use.

A special `obsRaw._json` will also be added, which is the entire JSON as a string, this is mainly for use in C# where you can deserialize this into an object for easier access/traversal.



# OBS raw
* [Tempory list of requests](https://github.com/Palakis/obs-websocket/blob/4.x-current/docs/generated/protocol.md#requests) 
* [Eventually the new one](/en/Integrations/OBS/OBS-Requests)
{.links-list}

---

## How does OBS raw work?

OBS raw is a JSON coding language, where you can change/get properties of OBS things. The things that you request doesn't have to be sources it can be anything OBS related.

## How does it look like?

Here a basic example.

```json
{
"request-type": "TheRequestType",
"sceneName": "your scene name",
"sourceSettings": {
"color": 4278255360,
"name": "your name",
 },
}
```

I'm gonna split everything above up in pieces so you understand what this means.

`{  }` The brackets these are essential in your OBS raw code the always should be at the beginning and the end of your code.

`"request-type": "TheRequestType"` The request type is needed to point out the request your making

`,` a comma at every end of a line except every opening bracket and the last closing bracket is needed.

If your doing a sub branch like `sourceSettings` or `filterSettings` you need to do it like this

```json
"sourceSettings": {
"color": 4279410288,
"name": "your name",
},
```
---

## Basic Example
#### Now you know how the basics work where gonna make a request that you're probably gonna use.

First you need to do the brackets.

```json
{

}
```

Then you need to add the request type.


```json
{
"request-type": "SetSourceSettings"
}
```

Then you need to know what elements your gonna use with [SetSourceSettings](https://github.com/obsproject/obs-websocket/blob/4.x-current/docs/generated/protocol.md#setsourcesettings) (all info in this link)

Now that you know what you can put it in

```json
{
"request-type": "SetSourceSettings",
"sourceName": "your source name",
"sourceSettings": {
 "": "",
 },
}
```

But to know what source settings exist you need to do GetSourceSettings

```json
"request-type": "GetSourceSettings",
"sourceName": "your source name",
```

Now that we know that for this color source we can change the color/height and width (these things are diffrent depending on the source)

```json
{
"request-type": "SetSourceSettings",
"sourceName": "your source name",
"sourceSettings": {
  "color": 4278190335
  "height": 500
  "width": 200
 },
}
```
color: Needs to be ABGR with the `Pick Color` sub-action you can convert the color to ABGR rather easily, It is a number so it doesn't need ""

height: It is a number so it doesn't need ""

width: It is a number so it doesn't need ""

## Tutorials for beginners


* [How To Send CUSTOM WEBSOCKET COMMANDS To OBS*by Andilippi*](https://youtu.be/4Lf0VTs14W4)
{.links-list}

<p align="left"><iframe width="280" height="158" src="https://www.youtube.com/embed/4Lf0VTs14W4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen"></iframe></p>