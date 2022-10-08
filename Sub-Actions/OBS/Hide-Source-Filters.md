---
title: Hide Source Filters
description: Hide your OBS / SLOBS Source Filters
published: true
date: 2022-10-07T12:08:45.026Z
tags: twitch, obs, slobs
editor: markdown
dateCreated: 2022-03-19T16:40:42.314Z
---

# Hide Source Filters

Streamer.Bot has the ability to link with OBS/SLOBS (Stream labs OBS) and control certain aspects like with this Source filter it can hide the source filter visibility using a Sub-Action in the bot. An example Source filters being the special effect filter for the web camera. 

### Pre-requirements 
So, for this to work you will need to have your Streamer.Bot linked to OBS/SLOBS. If you don’t have this setup head over to [OBS](/en/Integrations/OBS) or [SLOBS](/en/Integrations/SLOBS) to find out how. 

Make sure the status says it is connected. Otherwise, the Bot cannot perform this action.

![image_2022-03-30_192005.png](/hide-source-filters/image_2022-03-30_192005.png){.align-center}

### Hide Source Filters 

In OBS/SLOBS you will need to have a source with a filter just like the image below. 

![image_2022-04-03_051016.png](/hide-source-filters/image_2022-04-03_051016.png)

Next in Streamer.bot create an action or use an existing one next right click to get the Sub-Action menu displayed. Now navigate to `Add Action` then `OBS` then click the `Hide Sources Filter`. 

![source_filters.png](/hide-source-filters/source_filters.png)

Next you will see a pop-up box like the one below. In this box you will need to select the OBS/SLOBS connection you want the bot to send this command to. Now select the Scene of which the Source is in and finally the Source itself.
> This will hide ALL filters on the selected source! 
{.is-info}

![overview.png](/Sub-Actions/OBS/hide-sources-filters/overview.png =400x)

Once you’re done click the `Test` button and check back in OBS/SLOBS and you'll see it has set the source filter visibility to hidden.

![image_2022-04-03_052615.png](/hide-source-filters/image_2022-04-03_052615.png)

Click `OK` to Confirm the Sub-Action and that’s it you're done

---

- [<i class="mdi mdi-chevron-left"></i> **OBS Studio Sub-Actions *Go Back***](/en/Sub-Actions/OBS)
{.btn-grid .my-5}