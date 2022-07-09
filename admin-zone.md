---
title: admin zone
description: 
published: false
date: 2022-07-09T03:25:46.803Z
tags: 
editor: markdown
dateCreated: 2022-07-03T19:53:46.241Z
---

# Admin Zone
### A place for admins to test wiki things!
*[Mady by robophill](https://www.twitch.tv/robophill)*{.translation-badge}
> **This page is admin only**
{.is-admin}

> **THIS PAGE IS RADIOACTIVE!!!**
{.is-radioactive}

> A star is a luminous ball of gas, mostly hydrogen and helium, held together by its own gravity. Nuclear fusion reactions in its core support the star against gravity and produce photons and heat, as well as small amounts of heavier elements.
{.is-star}

> test
{.is-success}

> test
{.is-succesbetter}

*in-consideration*{.ideas-in-consideration}
*in-progress*{.ideas-in-progress}
*approved*{.ideas-approved}
*available*{.ideas-available}

- Grid Item 1
- Grid Item 2
- Grid Item 3
{.grid-list}

## code language
```csharp
using System;
using System.Net;
using System.Net.Http;
using Newtonsoft.Json;

public class CPHInline
{
	public bool Execute()
	{
	string discordWebhook = args["webhook"].ToString();
		string user = args["user"].ToString();
        string precolor = "#ff0000";
		int color = Convert.ToInt32(precolor.Substring(1), 16);
		string discordJson = JsonConvert.SerializeObject(new {embeds = new[] { new { title = $"{user} is banned", color = color, description = "" } } });
		MultipartFormDataContent dataContent = new MultipartFormDataContent();
		dataContent.Add(new StringContent(discordJson), "payload_json");
		HttpClient httpClient = new HttpClient();
		httpClient.PostAsync(discordWebhook, dataContent).Wait();
		httpClient.Dispose();	
	return true;
	}
}
```