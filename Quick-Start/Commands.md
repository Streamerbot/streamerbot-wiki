---
title: Quick Start - Chatbot Example
description: Learn how to configure some basic chat commands with Streamer.bot
published: true
date: 2022-07-28T00:36:03.207Z
tags: guides, quick-start
editor: markdown
dateCreated: 2022-07-10T01:47:22.629Z
---


# Overview

If you are coming from another bot platform, you are probably used to having some basic commands available out of the box.

Streamer.bot ships with a blank slate - but a few simple actions can provide similar functionality.

Below, you will find a code to import them directly into your setup for immediate use and also explanations on why the workflows are set up this way so you can build more advanced actions if you want them.

# Commands

The following commands will be imported into your Streamer.bot instance:

![ActionExamples](https://media.discordapp.net/attachments/880176943566299136/933519049042825216/unknown.png)
## Import Code

Click **Import** at the top of Streamer.bot and paste the following code into the **Import String** field:

```
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
```

You should then see the **Name** field populated with `Quick Start`, and numerous actions to import should now show in the list.

Click **Import** to finalize your selection and add all selected actions to your Streamer.bot installation.

---

- [<i class="mdi mdi-chevron-left"></i> **Quick Start Guide *Go Back***](/en/Quick-Start)
{.btn-grid .my-5}