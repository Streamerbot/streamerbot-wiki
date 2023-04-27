---
title: DonorDrive
description: Monitor charity donation events sent from the Donor Drive platform
published: true
date: 2023-04-27T14:27:40.121Z
tags: v0.1.5
editor: markdown
dateCreated: 2022-06-01T04:57:34.650Z
---

> Info and Documentation of DonorDrive can be found [here](https://www.donordrive.com/)
{.is-info}

## Overview
![donordrive-integration.png](/donordrive-integration.png)

## Variables
### Donation
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

### Incentive
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

### Profile Update
Name | Description
----:|:------------
`name` | the name of the profile
`teamName` | The name of the team
`eventName` | The name of the event
`goal` | The total goal
`donations` | An array of the donations
`raised` | The total amount of money that has been raised
`isTeam` | A `true`/`false` respone if this is a team
`isParticipant` | A `true`/`false` respone if the user is a participant

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/Integrations)
{.btn-grid .my-5}