---
title: Streamlabs
description: Streamer.bot integration with Streamlabs
published: true
date: 2022-07-08T19:11:01.336Z
tags: integrations, streamlabs
editor: markdown
dateCreated: 2021-08-25T21:32:50.615Z
---

![streamlabs-logo.png](https://streamer.bot/img/integrations/streamlabs.png){.align-abstopright}
# Overview

**Streamer.bot** can monitor your Streamlabs account and perform actions on Donation and Merchandise events.

![Streamlabs1](/130132998-c43b43a0-7a91-44f9-87ff-227b12b3c525.png =700x)

# Configuration

To enable Streamlabs integration you will need a `Socket API token` from [streamlabs.com](https://streamlabs.com/)

![Streamlabs2](/130133061-8a2cbf68-1613-4c74-acb3-ea62e6e08cd8.png)

# Events

Both `Donations` and `Merchandise` have access to a number of text [variables](/Variables) that can be passed to your [sub-actions](/Sub-Actions)

For donation events, different actions can be run based on the size of the donation. 

### Donations

| Variable | Description |
|---------:|:------------|
`donationFrom` | Who the donation was from, as the user filled out
`donationAmount` | the amount of the donation
`donationCurrency` | 3 letter currency code
`donationFormattedAmount` | The donation amount with the currency symbol
`donationMessage` | Any donation message the user may have included
`isTest` | Boolean value indicating if the donation was a test |  `True`/`False` 


### Merchandise

| Variable | Description |
|---------:|:------------|
`merchandiseFrom` | Who purchased a product
`merchandiseMessage` | Any message the user attached to the purchase
`merchandiseProduct` | The product that was purchased
`merchandiseImageUrl` | URL to the image of the product
`merchandiseImageEscaped` | URL to the image of the product with escaped characters
`isTest` | Boolean value indicating if the purchase was a test |  `True`/`False` 

