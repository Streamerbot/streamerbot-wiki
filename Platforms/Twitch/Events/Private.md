---
title: All (v0.1.14)
description: Twitch Events Reference
published: false
date: 2022-09-03T23:34:39.952Z
tags: 
editor: markdown
dateCreated: 2022-09-03T23:14:09.721Z
---

## Overview
In this tab you can assign actions to your Community Goal that you have set up through your Twitch dashboard. 

> **NOTE:**
> THIS DOESN'T CREATE THE COMMUNITY GOAL.
{.is-info}

To get to this tab you need to click through the following tabs, First click the `Settings` tab next click on the `Events` tab then finally click the `Community Goal` tab. You should now see a window just like the image below.

![communitygoal1.png](/communitygoal1.png =700x)

In the image above we have 2 options one is to add an action to each time a chatter has contributed to the community goal and the other is triggered when the Community Goal is Complete/Finished.

All you need to do is create an action of each of these and assign them to the relevant triggers `Contribution` or `Finished`

On the right side of this tab you have a test area where you can emulate/test the actions you have assigned to the relevant triggers.

## Variables
The following variables will be available from this event:

Name | Description
----:|:------------
`title` | Name of community goal
`goalAmount` | The total amount required to complete the goal
`goalAmountFormatted` | The total amount required to complete the goal, formatted
`contributed` | How much has been contributed to this goal so far
`contributedFormatted` | How much has been contributed to this goal so far, formatted
`percentComplete` | How far along the community goal is
`userContributed` | How much the user have contributed
`userContribFormatted` | How much the user  contributed as a formatted number
`userTotalContributed` | The total amount the user has contributed to this goal
`userTotalContribFormatted` | The total amount the user has contributed to this goal, formatted
{.vars-table}

Unverified variables - Mileage may vary
| Name | Description|
|-----:|:-----------|
`startedAt` | Date Time the community goal was started
`endedAt` | Date Time the community goal ends 
`daysLeft` | `endedAt` - Current Date Time
{.vars-table}

---

<div id="footer-grid" style="display: grid; grid-template-columns: 1fr 1fr; grid-gap: 20px; margin-top: 30px;"><a href="/en/Platforms/Twitch/Events" id="footer-grid-border" style="border: 1px solid #333333; border-radius: 12px; color: transparent!important;"><div id="footer-grid-border-spacing" style="margin: 10px;"><div id="footer-grid-1"><div id="footer-grid-upper" style="color: #ffffff; font-weight: 700;">Twitch Events</div> <div id="footer-grid-bottom" style="font-size: 10px; margin-top: 3px; color: #6e6e6e; font-weight: 500;">Go Back</div></div></div></a></div>