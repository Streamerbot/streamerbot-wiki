---
title: Donation
description: Streamlabs Triggers Reference
published: true
date: 2023-03-16T11:15:00.651Z
tags: 
editor: markdown
dateCreated: 2023-03-15T20:32:22.676Z
---

## Overview
This triggers when you get a donation via Streamlabs.

For a detailed guide about StreamElements see [this page](/Integrations/Streamlabs).

## Configuration
### Ranges
You can select ranges if you want to filter between two values.

## Variables
Name | Description
----:|:------------
`donationFrom` | Username of the user as provided by Streamlabs (may not be from Twitch)
`donationAmount` | The amount of the donation
`donationCurrency` | The 3 letter payment currency code
`donationFormattedAmount` | The donation amount with the currency symbol
`donationMessage` | The dontaion message that the user may has included
`isTest` | Boolean value indicating if the tip was a test `True`/`False`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Streamlabs Triggers Reference *Go Back***](/Triggers/Streamlabs)
- [<i class="mdi mdi-account primary--text"></i> **Merchandise *Next Up***](/Triggers/Streamlabs/Merchandise)
{.btn-grid .my-5}