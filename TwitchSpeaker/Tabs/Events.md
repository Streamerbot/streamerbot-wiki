---
title: Events
description: Twitch Speaker Event options 
published: true
date: 2023-01-20T15:06:19.912Z
tags: twitch, tts, events, twitchspeaker
editor: markdown
dateCreated: 2022-09-13T00:09:15.503Z
---

In the TwitchSpeaker Events Tab you will find a series of configurable event for the TTS

So, to get to this tab all you need to do is to open `TwitchSpeaker` then click the `Events` tab you will land on this page shown below.

![events-tab-overview.png](/twitchspeaker/tabs/events/events-tab-overviewv1.png =700x)

## Global Event Settings
First section of this tab you will see is a `Global Event Settings` here you will be able to see a `Voice Alias` that will complete all the events here unless specified otherwise. next to this is a check box that will enable the use of this voice or the generic one you have chosen for the TwitchSpeaker TTS to use for everything.

![global-event-voice-v1.png](/twitchspeaker/tabs/events/global-event-voice-v1.png =700x)

## Event States
In this section you have a check box to enable/disable the event triggers for TwitchSpeaker to announce along with additional options as seen in the screenshot below. You can specify the amount for Cheer, Donations, Raids and Hosts with (x) number of viewers.

> **Note: Hosts are now discontinued due to Twitch API changes. **
{.is-info}

![event-state-v1.png](/twitchspeaker/tabs/events/event-state-v1.png =300x)

---

## Per Event Settings
This section is where you can really customise TwitchSpeaker TTS with your own unique message and your flair and personality. also it doesn’t have to be just one single message. You can have multiple different messages for each event and TwitchSpeaker will choose one at random or you can add weight to each message (this makes it that TwitchSpeaker will favour 1 message more than the other that are available). In this section you also have a checkbox that allows you to Enable/Disable a specific message.

![per-event-setting-v1.png](/twitchspeaker/tabs/events/per-event-setting-v1.png =700x)
## Variables
Name | Description
----:|:------------
`name` | Say the name of the user who triggered the event
`level` | Say the current level of a Hype Train
`gift` | Say the amount of gift subs given to the community
`subtier` | Say the tier of the subscription
`title` | Say the title of the channel point reward redeemed
`cost` | Say the cost of the channel point redemption that has been triggered
`bits` | Say the number of bits cheered
`amount` | Say the amount bits / money / channel points used or donated
`percent` | Say the percentage of completion of a hype train or a community goal etc.
`currency` | Say the currency used in the donation message
`tier` | Say the tier of the Subscription gifted
`recipient` | Say who received a gift sub
`cumulative` | Say how long a user has been subscribed to the channel
`message` | Say the text that is pass through with a sub, resub or donation

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/TwitchSpeaker)
- [<i class="mdi mdi-exclamation-thick text--twitch"></i>**Custom Commands *Commands that you can create for TSS messages.***](/TwitchSpeaker/Tabs/Custom-Commands)
{.btn-grid .my-5}

