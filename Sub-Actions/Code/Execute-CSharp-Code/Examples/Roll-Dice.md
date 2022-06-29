---
title: Roll Dice Example
description: 
published: true
date: 2021-08-26T01:42:36.186Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:46.325Z
---

Here is the sample code for a roll dice command.

Create a new action, with an execute code sub-action containing the following, I would recommend enabling `pre-compile at start` as well.

Create a `!roll` command, with `start`, and point to the action you just created.

```csharp
using System;
using System.Security.Cryptography;
using Newtonsoft.Json.Linq;

public class CPHInline
{
    public bool Execute()
    {
        var msg = args["rawInput"].ToString();
        var user = args["user"].ToString();
        if (string.IsNullOrEmpty(msg))
        {
            CPH.SendMessage($"{user}, use !roll <count>d<size> [+<modifier>] to roll some dice!");
            return false;
        }

        msg = msg.Trim().ToLowerInvariant();
        var words = msg.Split(' ');
        if (words.Length == 0 || words.Length > 2)
        {
            CPH.SendMessage($"{user}, use !roll <count>d<size> [+<modifier>] to roll some dice!");
            return false;
        }

        var diceRoll = words[0];
        var diceRollValues = diceRoll.Split('d');
        if (diceRollValues.Length != 2)
        {
            CPH.SendMessage($"{user}, use !roll <count>d<size> [+<modifier>] to roll some dice!");
            return false;
        }

        if (!(int.TryParse(diceRollValues[0], out var count) && int.TryParse(diceRollValues[1], out var size)))
        {
            CPH.SendMessage($"{user}, use !roll <count>d<size> [+<modifier>] to roll some dice!");
            return false;
        }

		if (count < 1)
		{
			CPH.SendMessage($"{user}, well, uhh, umm, how am i suppose to roll {count} dice?");
			return false;
		}

		if (size < 0)
		{
			CPH.SendMessage($"{user}, what exactly is a {size}, I've never heard of that, are you from some wierd dimension?");
			return false;
		}

        var value = 0;
        for (var i = 0; i < count; i++)
        {
            value += CPH.Between(1, size);
        }

        var withAdded = false;
		int addedValue = 0;
        if (words.Length > 1 && words[1].StartsWith("+"))
        {
            if (int.TryParse(words[1].Replace("+", ""), out addedValue))
            {
                withAdded = true;
                value += addedValue;
            }
        }

        var text = diceRoll;
        if (withAdded) text += words[1];
        if (withAdded)
        {
            CPH.SendAction(" rolls " + text + " on behalf of " + user + " with a " + words[1] + " modifier, and tallies it up for " + value.ToString());
        }
        else
        {
            CPH.SendAction(" rolls " + text + " on behalf of " + user + ", studying them for a bit, and tallies them up for " + value.ToString());
        }

		CPH.SetArgument("diceValue", value);

		var jObject = new JObject();
		jObject["roll"] = value;
		if (withAdded)
		{
			jObject["modifier"] = addedValue;
			jObject["rollWithoutModifier"] = value - addedValue;
		}
		jObject["user"] = user;
		jObject["count"] = count;
		jObject["size"] = size;

		CPH.WebsocketBroadcastJson(jObject.ToString());

        return true;
    }
}
```