---
title: DonorDrive
description: Monitor charity donation events sent from the Donor Drive platform
published: true
date: 2022-09-12T15:41:12.091Z
tags: v0.1.5
editor: markdown
dateCreated: 2022-06-01T04:57:34.650Z
---

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

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}