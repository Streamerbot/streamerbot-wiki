---
title: Action Queues
description: Action Queues Allow you to run actions One by One without Overlap
published: true
date: 2022-09-11T18:41:37.913Z
tags: 
editor: markdown
dateCreated: 2022-07-12T11:08:52.458Z
---

# Overview

The `Action Queues` Tab allow you to see what actions are queued up, which actions have already ran and any queues you may have created.

Queues are Streamerbots way of lining up actions so they don't all run at once, you can have multiple queues so you can line up actions in separate  lines. One example of this would be if you had an Alert Queue and a SFX Queue. No 2 alerts or SFX will trigger at the same time, however an Alert and a SFX may Trigger at the same time.

> Queues run separately , so if you have 2 blocking queues and them actions are triggered at the same time they will run at the same time. Only Actions inside the one queue will be affected by the blocking {.is-warning}

## Pending Actions

Pending Actions will show your current list of actions waiting to run. These can be sorted by `Name`, `Queued At` or `Started At`. Once an action has been completed it will move to the `Action History` Tab.

![pendingactions.png](/pendingactions.png)

## Queues

This will show you your current list of queues and this is where you will add a queue. This will show you the the information regarding that queue. `Name`, `Pending Count`, `Completed Count`, `Paused` and `Blocking`

![queues.png](/queues.png)

> `Completed Count` is only counted while the bot is open - closing the bot will reset all values. {.is-info}

In order to add a queue you will right click and press Add, give your queue a Name, and select if you wish to have it as a blocking queue or non-blocking. 

> Ticking the box will make it a `Blocking Queue`, requiring each action to execute one-by-one with no overlap.
{.is-success}

![addqueue.png](/addqueue.png)

Once you've created a queue you can add actions to it on the Add/Edit actions popup

![new-action-dialogue-018.png](/new-action-dialogue-018.png)

## Action History

This is where you can view all previously ran actions. From here you can inspect Variables, before and after been ran. 
You can also requeue if you wish to re-run an action. 

![actionhistory.png](/actionhistory.png)

## Inspect Variables
In `Pending Actions` and `Action History` you can choose to inspect the variables this will show you all the variables that are available for that action, you can choose a before and after so you can see how the variables change if that is something that you wish.

![inspectvariables.png](/inspectvariables.png)

