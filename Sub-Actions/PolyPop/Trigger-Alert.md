---
title: Trigger Alert
description: PolyPop Sub-Actions Reference
published: true
date: 2023-03-27T18:36:00.251Z
tags: subactions, polypop
editor: markdown
dateCreated: 2022-06-27T21:28:06.392Z
---

## Overview
Limited PolyPop support is now available in Streamer.bot *v0.1.8+*{.version-badge}

This sub-action connects to PolyPop via WebSocket to trigger alerts.

![polypop-streamerbot-notconnected.png](/polypop/polypop-streamerbot-notconnected.png =700x)

## Prerequisites
1. [PolyPop](https://www.polypoplive.com)
2. Streamer.bot *v0.1.8+*{.version-badge}
3. Install the [PolyPop WebSocket Plugin](https://github.com/Jabbey92/PolyPopWebsocketPlugin/releases/tag/1.1)

## Configuration
Once you have installed the PolyPop WebSocket go ahead and open PolyPop and Streamer.bot (0.1.8) or later. Next in Streamer.bot navigate through the following tabs `Stream Apps` then in the second row of tabs click `PolyPop`.

In this tab click the `Auto Start` check box and leave the other setting as default next, click the `Start Server` button. just like the one below.

![polypop-streamerbot.png](/polypop/polypop-streamerbot.png =700x)

Next open the PolyPop application assuming you have already got a scene with some events and alerts already setup we next need to navigate to the `Open Library` button in the bottom left of the PolyPop application next you will see a pop-up window; you will see a windows just like the one below.

![polypop-library.png](/polypop/polypop-library.png =700x)

Next in the `Library` Section you will see a giant `+` button click this and menu will appear now click the `WebSocket` option this will now add this to the alert objects. but we need to configure this so select the WebSocket so it properties appears in the `Properties` pane.
![polypop-web-socket-library.png](/polypop/polypop-web-socket-library.png =600x)

In the `Properties` pane we need to point the WebSocket to Streamer.bot so if you used default settings you can change the **Port Number** in the properties to **9652**. Next, we need to amend the `Trigger Alert` section inside properties so here if you expand the `Trigger Alerts` section you see 2 input fields first one being `Alert title` and the Second being `Alert Value`.  Go ahead and fill these in but remember these as you will need to tell Streamer.bot these values.  Next you will see the `Alerts` section within the `Properties` pane you will need to click the small `+` button this will allow you give the alert trigger a name this will also need to be given to Streamer.bot. Next link the WebSocket to the action or scene that you want it to trigger. Just like the image below.
![polypop--config.png](/polypop/polypop--config.png =700x)

Now we need to create a sub action or amend an existing one and link it to a command or a redeem but we will just create the action for this. So, if you create an action or use an existing action then in the right pane you have sub actions from here you right click and navigate the following `Add Sub-Action` then down `PolyPop` then click `Trigger Alert` a dialog box like the one below will appear.

![polypop-ta-dialog.png](/polypop/polypop-ta-dialog.png)

In this Dialog box you to input the detail you have specified in the `WebSocket Properties` pane in the PolyPop application. so, the alert name you used in WebSocket properties pane need to match here and repeat this process for the variable name and the value. once completed click `Ok` now that the sub-action is made. You can tie this to a command / redeem via the Streamer.bot action.

![polypop-ta-complete.png](/polypop/polypop-ta-complete.png)

You have successfully linked Streamer.bot to PolyPop and configured the trigger via WebSocket.

![polypop-complete.png](/polypop/polypop-complete.png =700x)

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/Sub-Actions)
{.btn-grid .my-5}