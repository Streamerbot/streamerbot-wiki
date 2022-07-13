---
title: Polls
description: 
published: true
date: 2022-06-27T21:18:06.928Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:34.620Z
---

## Twitch Polls

With Twitch polls, you can drive interactive elements on your stream, showing your viewers choices in real time!  You could also create polls when certain actions happen, or setup some pre-defined polls, and just assign the actions to keys on your StreamDeck (or TouchPortal) for quick and easy access!

The usage of Polls within Streamer.bot can be a bit more complex, so be sure to ask in the Discord if you get stuck!

**Note** I do plan on adding a `Sub-Action` for creating polls, at least, it's on my list, so this will provide another path, other then the [C# Example](#basic-creation-example) shown below.

## Variables Available

| Variable | Description |
|      ---:|-------------|
| `poll.Id` | Twitch's ID for the poll |
| `poll.StartedAt` | When the poll was started |
| `poll.Title` | The title of the poll |
| `poll.Duration` | How long the poll will run for, in seconds |
| `poll.DurationRemaining` | How much longer the poll has left, in seconds |
| `poll.choices.count` | The number of choices |

### Choices available

| Variable | Description |
|      ---:|-------------|
| `poll.choice#.title` | The title of the poll choice |
| `poll.choice#.votes` | Number of regular votes for the choice |
| `poll.choice#.bitVotes` | Number of bit based votes for the choice |
| `poll.choice#.rewardVotes` | Number of reward based votes for the choice |
| `poll.choice#.totalVotes`| Total number of votes for the choice |

Replace the # in choice# with 0 to 4, depending how many choices there are, to get the choice entry

| Variable | Description |
|      ---:|-------------|
| `poll.votes` | Total number of regular votes |
| `poll.bitVotes` | Total number of bit based votes |
| `poll.rewardVotes` | Total number of reward based votes |
| `poll.totalVotes` | Overall total number of votes |

The above variables are available for all poll actions

`poll.EndedAt` is also available for the completed action

### Poll Ended Variables

| Value | Description |
|   ---:|-------------|
| `poll.winningIndex` | The index of the winning choice, from 0 to 4 |
| `poll.winningChoice.id` | The ID of the winning choice |
| `poll.winningChoice.title` | The title of the winning choice |
| `poll.winningChoice.votes` | Number of regular votes |
| `poll.winningChoice.bitVotes` | Number of bit based votes |
| `poll.winningChoice.rewardVotes` | Number of channel point based votes |
| `poll.winningChoice.totalVotes` | Total number of votes for the choice |
| `poll._json` | JSON string of complete event information that can be parsed

Because how some of this is handled, it is recommended that Execute C# code is used for these as some logic maybe required

**Note** if there are variables missing that you think maybe of benefit, let me know and I can likely add them in

## Basic Creation Example

Since the initial usage of creating polls currently requires [Execute C# Code](/Sub-Actions/Code/Execute-CSharp-Code), a simple example is provided below.  I've added a few comments to it which hopefully will help you get it setup for your usage.  If you still have questions, be sure to ask them in the discord!

### Code

```csharp
using System;
using System.Collections.Generic;

public class CPHInline
{
	public bool Execute()
	{
		// replace the text between the "" with the poll question
		string pollQuestion = "Which poll option is best?";

		// these are your poll options, you can have upto 5, if you don't want 5, just delete the lines you don't want, so say
		// you would like 2, delete Option 3, 4, and 5.
		// and be sure to rename your options by changing the text inbetween the ""
		string pollOptions = new List<string>();
		pollOptions.Add("Option 1");
		pollOptions.Add("Option 2");
		pollOptions.Add("Option 3");
		pollOptions.Add("Option 4");
		pollOptions.Add("Option 5");

		// change the number below to alter the duration of the poll, it is in seconds
		int duration = 60;

		// the next two are options, leave them at 0 to disable them, or, set them to a value to enable them
		int bitsPerVote = 0;
		int channelPointsPerVote = 0;

		CPH.TwitchPollCreate(pollQuestion, pollOptions, duration, bitsPerVote, channelPointsPerVote);

		return true;
	}
}
```

### Import String

For easier importing, here is an import string you can use, right click in `Actions`, and choose `Import`

```
TlM0RR+LCAAAAAAABAClVltzokgUft+q/Q9WntcsCMYwVfMgGgGjbMQEkHUeaLpFQnNZEBWm5r/vadAEdedhavNi6O9cvnPO15fvv//W6dztSZYHSXz3pdP7o16I3YjA190oI+6OdF4SSjtPRzdKKblrLFxvBx45GP3Nvjud780PQAFmroI7EMU+3++KvIi6In4Uuu4Dwl1u8Ig3D8JARH2piVU7/VOQgqWMC0o/V0nsIkpYvF1WkNb60aMFJpMsidQg3yVZCSYbl+Ytm8saWAmtdH6WFClD2XreAlx6cMvcKOLbgJkb4yQa1oXfol4Se0WWkXh3i90066Jh/8G26fgoweSTWm2GSe5lQXqicHeFhoSkQxrsyQ2FpgCyIUDQI1dManD0Zb22AqjwkK/X88DLkjzZ7O71p9f1epIBu0OShQ/ier0X77l7gRN4ab2Oci/JaIDucbu7/yfissx3JKrjtcN9u6wElTtSdwd6gG09RZHnvwm0woq5++vAPV+vzUJ9j5QjXQlGinr9ahZiiiKzdK35YLxI9FEs86vomK5K+R0pk8or5fHb03aKYA1Fb4Dn+igY+p5qBkih75oy3aPewTfsLcQ0OWfppxDH19TGThsN97NSLh1bzleWTjXVSJylzDn2lgNfilVMHUv0sbKl2kgLNBWnWPGbb1UGrgffs03q1XzFU0y5wuq0rstTpBxNJrxj65xrSYU25nyN4sS19OTsjwS5wRRasZyesPhTewd+PvcM/CDe477mZQM/ZVICvz4SzPLa3ysPPrEkXlP0LQrkZGU7wNE8YOXR15cH37VWJ9zYowBzUMsWxYsGi80Kj+TQsY4UK29NfQrrqVlpKt3jpRxCfTHYCCurz82gRlTK1coO230EXuDbk3ikLHzof+Ysh+WsFff1XOt4nmvjRQ71FM5oyM/atdZrcgB1VtiesplA/VPQwWT3UbsiQV10j+K5v4pDf9XbblGE6543szEoURdQcz9wbENwLLNoZjsMtHMu1dl6gXxAvWP++tHDoaQpfYpLee7CzF5UnfMiWjiVmDy/njVz7dOXHWWRaOGJUzA8akE4qHUGeWoNPH3wLRaWET6Ppi+eWmvGnwdayvZCw4nN9HjCmP4noTPyg1bfgl/gwf0KD33Z8Djbz8rHc1/P+6LAFg/91PxVZOZIYL0GG+vIsbVGMwbvRZOTnqXo5FfzBB2koJ8U9mwK+qwcC/Z6ZFTnfDAr7sIf9or+Pmz2/afGOBd0BLoUIRaHe5CfaeRTD6ApOD9q7UNuiwN84c/BFvQawky3cH6cMbCVmD4rB2wYf7Ss7bZMG0g1G+0pZrGypjk7F1w4oy75TlOs6gvHnlpIMCjjPB9/zCdl+6vpYZ+iibxnPh4vU486e7YfXpbDQ7vnC17WZtQQXNt4dye1FsZeZG7BNrk+S2Y38z/4jmqWK7ueZ37NDezfXdhb0Lv8TZGAm1G9KWZpRhKci2Grz+w8ZHOAc0+d8s5Jb5sF97xZfP16dZelGfGSKA3oTy4zTKhbLndudnvf1njzChEx5h94d9DFLr+Bp4jgdRG0qrvpiwLaSBIaPHBXiQ8k8LcsKHfPXSK7MmVkJPZ3iZyfExevlxr5yQumoRhjcmSJPld/nP/9dv16UFiK+uL+1n50UOqmOcEttAHrQI1l87ZquYJbFMFj5mz/418dveu9BgoAAA==
```