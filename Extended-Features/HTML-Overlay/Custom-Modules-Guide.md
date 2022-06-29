---
title: HTML Overlay Custom Modules Guide
description: Learn how to add new features to the HTML Overlay using Javascript
published: true
date: 2022-01-07T18:19:27.300Z
tags: html overlay, extended features, guides
editor: markdown
dateCreated: 2022-01-07T17:14:12.750Z
---

In this guide we are going to walk through a basic example module for the [**HTML Overlay**](/Extended-Features/HTML-Overlay) application, displaying a configurable image on your screen as a channel points reward.

## Create your JS Module

1. Create a new `.js` file in the `Content` directory. We are going to name this module `image-reward.js`;
2. Open `image-reward.js` in your preferred code editor. (*I will be using Visual Studio Code*)

3. Add the following code to the top of your module to read in configuration params:
    ```js
    // Get config from import params
    const url = new URL(import.meta.url);
    const config = {
      // this must match the title of the Channel Points reward we want to trigger for
      rewardTitle: url.searchParams.get('rewardTitle'),
      
      // this is the URL of the image we want to display
      imageUrl: url.searchParams.get('imageUrl'),
      
      // this is the number of seconds to display the image (defaults to 5)
      seconds: Number(url.searchParams.get('seconds')) || 5
    }
    ```
   
## Subscribe to Channel Point Rewards

1. Add the following code to your module to subscribe to Channel Point Rewards events:
    ```js
    window.streamerbot.subscribeTo({
      Twitch: [ "RewardRedemption" ]
    });
    ```
2. Next, add the code to listen to the specific Channel Point Reward for this module:
    ```js
    window.streamerbot.onMessage(message => {
      if (
        message.event.source === "Twitch" &&
        message.event.type === "RewardRedemption" &&
        message.data.title === config.rewardTitle
      )
        // This function is called anytime a Channel Point Reward is redeemed with a name matching our rewardTitle configuration
        // We will be creating this function in the next steps
        showImage();
    });
    ```
    
## Write your Action Function

1. Since this module will be showing an image on the screen as a reward, we are calling our function `showImage`
2. Within `showImage`, we will write the code to perform the action:
    ```js
    function showImage() {
      // Create our image element
      const imgElement = document.createElement("img");

      // Modify the image element src to point at the configured image URL
      imgElement.src = config.imageUrl;

      // Append the image element to the HTML document
      document.body.appendChild(imgElement);

      // Set a timeout to remove the image after the configured amount of time
      setTimeout(() => {
        imgElement.remove();
      }, config.seconds * 1000)
    }
    ```
    
## The Module Code

At this point, `show-image.js` should look something like this:

```js
// Get config from import params
const url = new URL(import.meta.url);
const config = {
  rewardTitle: url.searchParams.get('rewardTitle'),
  imageUrl: url.searchParams.get('imageUrl'),
  seconds: Number(url.searchParams.get('seconds')) || 5 // default to 5 seconds
}

// Will subscribe to these events, mapped directly to the websocket subscription request.
window.streamerbot.subscribeTo({
  Twitch: [ "RewardRedemption" ]
});

// Called when any event is received from Streamerbot, including those subscribed to by other scripts.
window.streamerbot.onMessage(message => {
  if (
    message.event.source === "Twitch" &&
    message.event.type === "RewardRedemption" &&
    message.data.title === config.rewardTitle
  ) {
    showImage();
  }
});

function showImage() {
  // Create our image element
  const imgElement = document.createElement("img");

  // Modify the image element src to point at the configured image URL
  imgElement.src = config.imageUrl;

  // Append the image element to the HTML document
  document.body.appendChild(imgElement);

  // Set a timeout to remove the image after the configured amount of time
  setTimeout(() => {
    imgElement.remove();
  }, config.seconds * 1000)
}
```

## Import your Module

Now, to include our module in the HTML Overlay application, we must import it from the `index.html` document.

1. Open `index.html` in your code editor. (*This file is also in the `Content` directory*)
2. At the end of `index.html`, before the trailing `</body>` tag, add the following code to import our module:
    ```html
    <script type="module" src="show-image.js?rewardTitle=DEE&imageUrl=https://streamer.bot/logo.png&seconds=2"></script>
    ```
  
  	You'll notice that we are passing in our configuration options as parameters on the module URL.
  
    ```js
    // show the image when someone redeems our channel point reward named 'DEE'
    rewardTitle: 'DEE'

    // display the streamer.bot logo
    imageUrl: 'https://streamer.bot/logo.png' 

    // show the image for 2 seconds
    seconds: 2
    ```

## Test

Now that everything is ready to go, we can test by running `HTMLWindowsOverlay.exe`
*Close HTML Overlay first if it is already running in the system tray*

When you go to your chat and redeem the Channel Point Reward with the name `DEE`, you should see the Streamer.bot logo pop up on your desktop!

