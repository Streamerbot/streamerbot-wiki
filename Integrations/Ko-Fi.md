---
title: Ko-Fi
description: Integrate Streamer.bot with your Ko-Fi account!
published: true
date: 2022-08-29T06:48:56.627Z
tags: integrations, ko-fi, v0.1.8
editor: markdown
dateCreated: 2022-06-01T04:37:51.447Z
---

![ko-fi_icon_rgb_rounded.png](/ko-fi_icon_rgb_rounded.png){.align-abstopright}

## Overview
Ko-Fi, a highly requested integration, is now available in Streamer.bot *v0.1.8*{.version-badge}

> **NOTE**
> This integration requires signing in to the **Streamer.bot** website and configuring your Ko-Fi account to use the webhooks.
{.is-info}

![kofi-integration.png](/kofi-integration.png)

## Configuration
To configure Kofi:

1. Head over to [Streamer.bot](https://streamer.bot), and click the `Sign In` button in the top right.
2. Authorize the login using your `Discord` credentials
3. When you've returned to the Streamer.bot website, click your profile icon in the top right, and click `User Settings`
4. You will see a list on the middle left of your screen with `General`, `Kofi`, and `Patreon`; you will want to click on `Kofi`
5. Copy the `Kofi Webhook Url`, and goto your [Kofi Account Page](https://ko-fi.com/manage/webhooks?src=sidemenu)
6. Paste the webhook you copied into the WebHook Url box, and click update
7. Click on `Advanced` to expand verification token information.
8. Copy this verification token, and go back to the Streamer.bot page, and paste it in the `Kofi Verification Token` box.
9. As a last step, make sure `Enabled` is toggled at the top of this page

> Be sure the Streamer.bot website integration is connected!
{.is-info}

## Events
### Donation
This event is triggered when a donation happens through Kofi

Name | Description
----:|:------------
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The amount donated |
| `currency` | The currency of the donation |

### Subscription
This event is triggered when a subscription happens through Kofi

Name | Description
----:|:------------
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The subscription amount |
| `currency` | The currency of the subscription |
| `tier` | The tier of the subscription |

### Resubscription
This event is triggered when a resubscription happens through Kofi

Name | Description
----:|:------------
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The subscription amount |
| `currency` | The currency of the subscription |
| `tier` | The tier of the subscription |

### Shop Purchase
This event is triggered when a shop purchase happens through Kofi

Name | Description
----:|:------------
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The amount of the purchase |
| `currency` | The currency of the purchase |
| `itemCount` | The currency of the donation |
| `item#` | The id of the item purchased, where # is the index of the item |

### Commissions
This event is triggered when a commission is purchased on Kofi

Name | Description
----:|:------------
| `messageId` | Kofi's internal ID |
| `timestamp` | Timestamp of when the event occured |
| `from` | Username of who triggered the event |
| `isPublic` | True/False of whether or not the message should be shared publicly |
| `message` | Message the user left |
| `amount` | The commission amount |
| `currency` | The currency of the commission |

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}