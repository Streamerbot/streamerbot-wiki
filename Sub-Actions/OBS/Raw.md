---
title: Raw
description: OBS raw is powerfull tool to do OBS things that you can't do in regular sub-actions.
published: true
date: 2023-03-16T11:40:32.501Z
tags: 
editor: markdown
dateCreated: 2022-08-20T18:39:46.278Z
---

With OBS Raw, you can send raw JSON requests directly to the OBS WebSocket connection, allowing you to make any OBS requests that are not already available as first-class [sub-actions](/Sub-Actions/OBS)

## Result/Variables
To use variables in the JSON request, add the % variable surrounded by quotes, it must still be valid JSON to parse properly.  The variable will be auto-typed when it is parsed to be sent to OBS, so if the variable is a number, the resulting JSON will not have double quotes around the value.

When the OBS Raw is executed, result will be places in the argument stack for the action.

Since the result is returned in JSON, it will walk the entire tree, and add each value as a `obsRaw.<JSON Path>` for use.

A special `obsRaw._json` will also be added, which is the entire JSON as a string, this is mainly for use in C# where you can deserialize this into an object for easier access/traversal.

## Tabs
### Raw
The raw code is in `JSON` and you need to follow the list of [Requests](/Broadcasters/OBS/Requests), and put those request fields in the `requestData` object.

![obsraw-menu-raw-default.png](/broadcasters/obs/raw/raw/obsraw-menu-raw-default.png)

### Preview
In the preview you see your raw code visually.

![obsraw-menu-preview.png](/broadcasters/obs/raw/preview/obsraw-menu-preview.png)

### Result
When you have clicked on the `Test` button you will see all the Response Fields/Variables.

![obsraw-menu-result-request-getversion.png](/broadcasters/obs/raw/result/obsraw-menu-result-request-getversion.png)

### Options
Here you see one parameter, `Add results to arguments`. 
When enabled, Streamer.bot will treat your `Result` as variables, by default this is turned on.

![obsraw-menu-options.png](/broadcasters/obs/raw/options/obsraw-menu-options.png =500x)

## Configuration
#### Name
Give this a name to sort it between the other sub-action (for example you can use your request type).

#### Variable Prefix
This will be in front of your variables when an action has ran.

#### Format
Using this button your raw code will automatticly be JSON formatted.

#### Test
This will test the raw code, but this won't run the action/sub-action in any way.

#### Connection
You can change between obs connections, more for advanced users.

***

### Format
```json
{
  "requestType": "request method",
  "requestData": { ... }
}
```
You can use this offical OBS raw generator by Streamer.bot
- [<i class="mdi mdi-application text--obs"></i>**OBS Raw Generator *Generate Streamer.bot OBS Raw requests for OBS Studio v28 and OBS WebSocket v5***](https://obs-raw.streamer.bot)
{.btn-grid .my-5}

---

Or you can find all the request fields on the OBS raw Requests page
- [<i class="mdi mdi-frequently-asked-questions text--obs"></i>**OBS Raw Requests *Reference of all requests supported with OBS Raw***](/Broadcasters/OBS/Requests)
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio Sub-Actions *Go Back***](/Sub-Actions/OBS)
{.btn-grid .my-5}