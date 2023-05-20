---
title: Donation
description: DonorDrive Triggers Reference
published: true
date: 2023-04-27T14:31:25.628Z
tags: 
editor: markdown
dateCreated: 2023-03-15T22:09:59.903Z
---

## Overview
This triggers when you get a donation via DonorDrive.

For a detailed guide about DonorDrive see [this page](/Integrations/DonorDrive).

## Configuration
### DonorDrive
Select any or a DonorDrive provider as the source for this donation.

## Variables
Name | Description
----:|:------------
`donorName` | The name of the donor
`donorAvatarUrl` | The URL of the donor's avatar
`donorIsAnonymous` | A `true`/`false` respone if the donor is anonymous
`recipientName` | The broadcaster's name used in the DonorDrive
`donorMessage` | The message of the donor
`donorAmount` | The amount that the donor has given
`isTeam` | A `true`/`false` respone if this is a team
`isParticipant` | A `true`/`false` respone if the user is a participant
`profileName` | The name of the profile
`profileTeamName` | The name of the profile's team
`eventName` | The name of the event
`goal` | The total goal
`donations` | An array of the donations
`raised` | The total amount of money that has been raised
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**DonorDrive Triggers Reference *Go Back***](/Triggers/DonorDrive)
- [<i class="mdi mdi-refresh primary--text"></i> **Incentive *Next Up***](/Triggers/DonorDrive/Incentive)
{.btn-grid .my-5}