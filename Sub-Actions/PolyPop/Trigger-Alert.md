---
title: Trigger-Alert
description: 
published: true
date: 2022-07-05T20:10:20.738Z
tags: 
editor: markdown
dateCreated: 2022-06-27T21:28:06.392Z
---

# Trigger Alert
With Streamer.bot 0.1.8 came PolyPop integration although its's limited. It's currently limited due to PolyPop still in it's infancy,but we can trigger some cool things via web-socket connection and a little configuration. 

![polypop-streamerbot-notconnected.png](/polypop/polypop-streamerbot-notconnected.png){.align-center}

## Pre Requirements
1. First, make sure you have PolyPop installed 
2. Second, make sure your version of Streamer.Bot is 0.1.8 or later.
3. Install the PolyPop web-socket add in which can be found [here](https://github.com/Jabbey92/PolyPopWebsocketPlugin/releases/tag/1.1)

## Getting it connected with Streamer.bot
Once you have installed the PolyPop web-socket go ahead and open PolyPop and Streamer.bot (0.1.8) or later . Next in Streamer.bot navigate through the following tabs `Stream Apps` then in the second row of tabs click `PolyPop`.

In this tab click the `Auto Start` check box and leave the other setting as default next, click the `Start Server` button. just like the one below.

![polypop-streamerbot.png](/polypop/polypop-streamerbot.png){.align-center}

Next open the PolyPop application assuming you have already got a scene with some events and alerts there setup we next need to navigate to the `Open Library` button in the bottom left of the PolyPop application next you will see a pop up window, you will see a windows just like the one below. 

![polypop-library.png](/polypop/polypop-library.png){.align-center}

Next in the `Library` Section you will see a  giant `+` button click this and menu will appear now click the `WebSocket` option this will now add this to the alert objects. but, we need to configure this so select the websocket so it properties appears in the `Properties` pane 
![polypop-web-socket-library.png](/polypop/polypop-web-socket-library.png)

In the properties pane we need to point the websocket to Streamer.bot so if you used default settings you can change the **Port Number** in the propties to **9652**. Next we need to amend the `Trigger Alert`
![polypop--config.png](/polypop/polypop--config.png)

Now we need to create a sub action or amend an existing one and link it to a command or a redeem but we will just create the action for this. So if you create an action or use an existing action then in the right pane you have sub actions from here you right click and navigate the following `Add Sub-Action` then down `PolyPop` then click `Trigger Alert` a dialog box like the one below will appear.

![polypop-ta-dialog.png](/polypop/polypop-ta-dialog.png){.align-center}
![polypop-ta-complete.png](/polypop/polypop-ta-complete.png)





![polypop--config.png](/polypop/polypop--config.png)
> More details coming soon...
{.is-info}
