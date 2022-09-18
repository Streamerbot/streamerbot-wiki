---
title: Streamlabs
description: Streamer.bot integration with Streamlabs
published: true
date: 2022-09-18T15:41:57.895Z
tags: integrations, streamlabs
editor: markdown
dateCreated: 2021-08-25T21:32:50.615Z
---

![streamlabs-logo.png](https://streamer.bot/img/integrations/streamlabs.png){.align-abstopright}

## Overview
**Streamer.bot** can monitor your Streamlabs account and perform actions on Donation and Merchandise events.

![overview.png](/intergrations/streamlabs/tabs/events/overview.png =700x)

## Configuration
To enable Streamlabs integration you will need a `Socket API token` from [streamlabs.com](https://streamlabs.com/)

![overview.png](/intergrations/streamlabs/tabs/settings/overview.png =700x)

## Events
Both `Donations` and `Merchandise` have access to a number of text [variables](/Variables) that can be passed to your [sub-actions](/Sub-Actions)

For donation events, different actions can be run based on the size of the donation. 

## Variables
### Donations
Name | Description
----:|:------------
`donationFrom` | Who the donation was from, as the user filled out
`donationAmount` | the amount of the donation
`donationCurrency` | 3 letter currency code
`donationFormattedAmount` | The donation amount with the currency symbol
`donationMessage` | Any donation message the user may have included
`isTest` | Boolean value indicating if the donation was a test | `True`/`False`

### Merchandise
Name | Description
----:|:------------
`merchandiseFrom` | Who purchased a product
`merchandiseMessage` | Any message the user attached to the purchase
`merchandiseProduct` | The product that was purchased
`merchandiseImageUrl` | URL to the image of the product
`merchandiseImageEscaped` | URL to the image of the product with escaped characters
`isTest` | Boolean value indicating if the purchase was a test | `True`/`False` 

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}