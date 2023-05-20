---
title: Google Cloud Service
description: TwitchSpeaker Speech Engines Reference
published: true
date: 2023-01-20T15:08:09.556Z
tags: 
editor: markdown
dateCreated: 2022-08-14T20:31:16.498Z
---

Go to Google Cloud Services, you can setup a free account and get a trial which lasts for 12 months, but there are limits.

1. Go to API & Services (Dashboard)
2. Click Cloud Text-to-Speech API
3. Click Enable API
4. Go to API & Services -> Credentials
5. Create Credentials
6. Pick Service Account
7. Enter a service account name, i.e. tts
8. Click Create
9. Click Continue (no roles)
10. Click +Create Key, pick JSON then Create, save this JSON FILE!
11. Click Done
12. Point to this JSON file for Google Auth in the TTS Settings tab, and you can now use the Google engine

> Google Cloud Services is a paid service, so **BE AWARE** of your usage/expirations.
>
> **Google Cloud Text To Speech Free Limits**
Standard (non-WaveNet) voices up to 4 million characters per month, and WaveNet voices are up to 1 million characters per month. Character counts include SSML tags, which the application does use, so, you can't go by just the normal text alone.
>
> WaveNet and non-WaveNet voices are indicated in the voice selections.
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/TwitchSpeaker)
{.btn-grid .my-5}