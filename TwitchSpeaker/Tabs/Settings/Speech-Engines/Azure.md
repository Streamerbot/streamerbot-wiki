---
title: Cloud Service Microsoft Azure
description: 
published: true
date: 2022-10-17T07:59:38.741Z
tags: 
editor: markdown
dateCreated: 2022-10-17T07:57:46.725Z
---

Since OneCore has been removed, it is technically replaced with the cloud services counterpart.

To setup this service, you are going to need a Microsoft Azure account, once you have an account head over to portal.azure.com

1. Click Create a Resource
2. Search for Speech in the search box, and pick it
3. Click "Create"
4. Enter a name, this must be unique, for example, I just called mine nate1280-tts
5. Pick your subscription (you may have to start the free trial, or if you have already done this, your service will be Pay-As-You-Go)
6. Pick your location, I use East US, this location can effect what voices are available for you.
7. Pick your pricing tier, you waant to pick the F0 Free Tier
8. Pick your resource group, if you do not have any setup, click "Create New" and add a new one
9. When all done, click the "Create" button at the bottom.
10. This takes a few moments to get setup, once its done, goto the newly created service and click on "Click here to manage keys"
11. You'll want to copy "KEY 1", and paste this into the subscription key box in Twitch Speaker
12. Copy the location, and paste it in the service location box
13. Click the Azure button to enable the engine and be sure to save your settings.
14. The free tier allows for 5 million characters per month with standard voices, and 500k characters per month for neural voices.

There is an option/ability to setup your own custom voice, but that is beyond the scope of this.

---

- [<i class="mdi mdi-chevron-left"></i>**TwitchSpeaker *Go Back***](/en/TwitchSpeaker)
{.btn-grid .my-5}