---
title: Incentive
description: DonorDrive Triggers Reference
published: true
date: 2023-04-27T14:31:18.482Z
tags: 
editor: markdown
dateCreated: 2023-04-27T14:31:16.154Z
---

## Overview
This triggers when you get an incentive via DonorDrive.

For a detailed guide about DonorDrive see [this page](/Integrations/DonorDrive).

## Configuration
### DonorDrive
Select any or a DonorDrive provider as the source for this donation.

## Variables
Name | Description
----:|:------------
`donorAvatarUrl` | The avatar url of the donor.
`donorIsAnonymous` | Wheter the donor is anonymous. Returns `True` or `False`.
`created` | The timestamp this incentive was created.
`recipientName` | The recipient of this incentive.
`donorMessage` | The message from the donor.
`donorAmount` | The donor amount.
`isTeam` | Wheter the recipient is a team. Returns `True` or `False`.
`isParticipant` | Wheter the recipient is a participant. Returns `True` or `False`.
`profileName` | The user name from the recipient.
`profileTeamName` | The team name from the recipient. Can be null.
`eventName` | The DonorDrive event name.
`goal` | The goal amount.
`raised` | The raised money for this goal.
`isIncentive` | Wheter the event is an incentive. Returns `True` or `False`.
`incentive.id` | The id of this incentive.
`incentive.isActive` | Wheter the incentive is active. Returns `True` or `False`. 
`incentive.amount` | The amount of the incentive.
`incentive.description` | The description of the incentive.
`incentive.image` | The image for the incentive. Can be an empty string.
`incentive.quantity` | The quantity of the incentive. Can be -1.
`incentive.quantityClaimed` | The amount of claimed quantity.
`incentive.links.donate` | The url of the donate link.
`incentive.startDate` | The timestamp this incentive starts.
`incentive.endDate` | The timestamp this incentive ends.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**DonorDrive Triggers Reference *Go Back***](/Triggers/DonorDrive)
- [<i class="mdi mdi-account-cog primary--text"></i> **Profile Updated *Next Up***](/Triggers/DonorDrive/Profile-Updated)
{.btn-grid .my-5}