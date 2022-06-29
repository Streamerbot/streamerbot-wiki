---
title: Predictions
description: 
published: true
date: 2022-06-24T00:47:35.998Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:38.706Z
---

## Prediction Variables

| Variable | Description |
|      ---:|-------------|
| `%prediction.Id%` | Twitch's ID of the prediction |
| `%prediction.CreatedAt%` | When it was created |
| `%prediction.Title%` | It's title |
| `%prediction.PredictionWindow%` | the duration of the prediction, in seconds |

### Outcomes available

| Variable | Description |
|      ---:|-------------|
| `%prediction.outcome#.id%` | Twitch's ID for the prediction |
| `%prediction.outcome#.title%` | Title for the prediction |
| `%prediction.outcome#.users%` | How many users picked this outcome |
|`%prediction.outcome#.points%` | Total number of rewards used |
| `%prediction.outcome#.color%` | The rgb hex color |

Replace the # in outcome# with 0 or 1, to get the outcome entry

The above are available for all prediction events

The two additional variable are availabe for `Completed`, `Pending` and `Locked` events

| Variable | Description |
|      ---:|-------------|
| `%prediction.LockedAt%` | When it was locked |
| `%prediction.EndedAt%` | When it ended |

Because how some of this is handled, it is recommended that Execute C# code is used for these as some logic maybe required

**Note** if there are variables missing that you think maybe of benefit, let me know and I can likely add them in

## Basic Creation Example

To create a prediction outside of the UI, you will need to use [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code), a simple example is provided below.  I've added a few comments to it which hopefully will help you get it setup for your usage.  If you still have questions, be sure to ask them in the discord!

### Code

```csharp
using System;
using System.Collections.Generic;

public class CPHInline
{
	public bool Execute()
	{
		// replace the text between the "'s with the prediction title
		var predictionTitle = "Which prediction option is best?";

    // these are your prediction options, you can have upto 10, if you don't want 10, just delete the lines you don't want, so say
    // you would like 2, delete Option 3, 4, 5, 6, 7, 8, 9 and 10
    // and be sure to rename your options by changing the text inbetween the "'s
    var predictionOptions = new List<string>();
    predictionOptions.Add("Option 1");
    predictionOptions.Add("Option 2");
    predictionOptions.Add("Option 3");
    predictionOptions.Add("Option 4");
    predictionOptions.Add("Option 5");
    predictionOptions.Add("Option 6");
    predictionOptions.Add("Option 7");
    predictionOptions.Add("Option 8");
    predictionOptions.Add("Option 9");
    predictionOptions.Add("Option 10");

    // change the number below to alter the duration of the prediction, it is in seconds
    var duration = 60;

    CPH.TwitchPredictionCreate(predictionTitle, predictionOptions, duration);

		return true;
	}
}
```