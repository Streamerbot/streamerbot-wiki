---
title: Merchandise
description: Streamlabs Triggers Reference
published: true
date: 2023-03-16T11:15:24.473Z
tags: 
editor: markdown
dateCreated: 2023-03-15T20:35:37.414Z
---

## Overview
This triggers when someone buys your merchandise from Streamlabs.

For a detailed guide about StreamElements see [this page](/Integrations/Streamlabs).

## Variables
Name | Description
----:|:------------
`merchandiseFrom` | Username of the user as provided by Streamlabs (may not be from Twitch)
`merchandiseMessage` | The message that the user may has included
`merchandiseProduct` | The product that was purchased
`merchandiseImageUrl` | The URL to the image of the product
`merchandiseImageEscaped` | The URL to the image of the product with escaped characters
`isTest` | Boolean value indicating if the tip was a test `True`/`False`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Streamlabs Triggers Reference *Go Back***](/Triggers/Streamlabs)
- [<i class="mdi mdi-cash primary--text"></i> **Donation *Next Up***](/Triggers/Streamlabs/Donation)
{.btn-grid .my-5}