---
title: Profile Updated
description: DonorDrive Triggers Reference
published: true
date: 2023-04-27T14:30:30.526Z
tags: 
editor: markdown
dateCreated: 2023-03-15T22:12:32.227Z
---

## Overview
This triggers when a profile is updated in DonorDrive.

For a detailed guide about DonorDrive see [this page](/Integrations/DonorDrive).

## Configuration
### DonorDrive
Select any or a DonorDrive provider as the source for this event.

## Variables
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
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**DonorDrive Triggers Reference *Go Back***](/Triggers/DonorDrive)
- [<i class="mdi mdi-cash primary--text"></i> **Donation *Next Up***](/Triggers/DonorDrive/Donation)
{.btn-grid .my-5}