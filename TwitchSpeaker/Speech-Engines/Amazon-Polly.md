---
title: Amazon Polly
description: TwitchSpeaker Speech Engines Reference
published: true
date: 2023-01-20T15:08:18.656Z
tags: 
editor: markdown
dateCreated: 2023-01-05T02:17:11.130Z
---

First you will need an Amazon AWS account, you can also setup a free trial. This lasts for 12 months. Once you have the account setup follow the steps below.

1. Log in to your AWS account.
2. After you’ve logged in, click Services from the top menu bar, then type IAM in the search box. Click IAM when it pops up.
3. On the left, click Users
4. Click Add User
5. Type in polly-windows-user (you can use any name)
6. Click the Programmatic access check box and leave AWS Management Console access unchecked
7. Click Next: Permissions
8. Click Attach existing policies directly
9. At the bottom of the page, in the search box next to Filter: Policy type, type polly
10. Click the check box next to AmazonPollyReadOnlyAccess
11. Click Next: Tags
12. Click Next: Review
13. Click Create user
14. IMPORTANT You need to copy the Access Key ID and the Secret Access Key (make it visible by clicking show)
15. Using those 2 keys, enter them in the TTS Settings in the app and you can now add the Amazon Polly Engine

NOTE It might take a couple hours for your Amazon account to be completely active, as it has to do a credit card verification even though its a free tier.

> Amazon Polly is a paid service, so **BE AWARE** of your usage/expirations.
>
> **AWS Free Tier Limits**
> For Amazon Polly’s Standard voices, the free tier includes 5 million characters per month for speech or Speech Marks requests, for the first 12 months, starting from your first request for speech. For Neural voices, the free tier includes 1 million characters per month for speech or Speech Marks requests, for the first 12 months, starting from your first request for speech.
>
> Neural and normal voices are indicated in the voice selections.
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/TwitchSpeaker)
{.btn-grid .my-5}