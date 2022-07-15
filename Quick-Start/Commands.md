---
title: Quick Start - Chatbot Example
description: Learn how to configure some basic chat commands with Streamer.bot
published: true
date: 2022-07-10T02:13:06.653Z
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

<section class="btn-grid my-5">

[<i class="mdi mdi-chevron-left"></i> **Quick Start Guide *Go Back***](/en/Quick-Start)

</section>