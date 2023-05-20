---
title: Importing & Exporting
description: 
published: true
date: 2022-11-15T22:51:28.916Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:05.659Z
---

Importing and Exporting Packages are the way to share projects that have been made with other members of the community, since 0.1.8 this has been updated to make it far easier with the addition of the ability to export commands too. 

## Exporting Actions and Commands

In the Top Left of Streamer.bot you will see an `Export` button.

![exportbutton.png](/exportbutton.png)

Pressing that will bring up this dialogue box.

![exportdialogue.png](/exportdialogue.png)

From here you can select one or more `Actions` and `Commands` you would like to package for export.

After selecting the actions and commands for your package, give it a name and then choose one of the buttons below

`Export to to Clipboard` will copy a string of UUEncoded text to the clipboard and show a confirmation dialogue. 

`Export to File` Will perform the same operation but automatically bring up a Save dialogue and create a file ready for transport

Exported actions will retain any custom JSON or C# code and will retain the sub-actions, group names and custom `Queues` an action was associated with. When actions are re-imported, Streamerbot will attempt to rebuild connections with OBS objects that match but these sub-actions may require opening up to confirm they are pointing to te intended sources

*** 

#### UUEncoded Action Example

```
TlM0RR+LCAAAAAAABADdV02P2zYQvRfofxAM5LZT8FtkbosUKHLpIYdcihyGnGFiwJa3spRkEeS/l7T2w2t7kXXjLJycJHHI4czjm3nUl99/a5rZR+7X81U3e9nIi81Ah0suX7M/GYcPzavV2A3czyYbpqHMXRfzP/W7ab5Mj2KaU12kddAqtBYoBw+m9RIC2gCqlUlmK7wRdvK1WfTvyGPdrBsXi/tR7jAuuPob+pHvxx9EdhMYvBr7nrthy+n7fjVe7TnFxSe8Xr8Za6YZF+stvz12tFpebnLbt6ZVl2722LPt4fEAk82U9WrsUw1bXDwY/4j9vKb5901SVJNK22jfTb2qR7Qe9hHZWInXw7zDGsjbG5/f8EeccVwMb3ExHghsOkiKPtlgHESU5SBTQEDvDLQuGZkpqGjsjttPPH//oYIk/thxOVxf1Y2kkg/HD57UFERH/Lm6uh/9evEYxAN/rtvObqjQTMzd5P6yebENxItdZHvOXBbRZdrMeAyNrNEqYxEcClHQiBrQFG57xUgBMTrfHo2GOBYMuQXG7eu7XTL+Vd1sGPlustzitluqGbWN5DygRgNGOgXImiDZJNCQaD2605bqJdHZlukth7a408y71DOumZphdSIi+UAYPWUIkkIhUmohxLa8OUqJQ0Ktjy+ro4mkn1JVP2njwuRCsOghciy0FmwAlRcgtM3kbWozp3NpXFsI/ECc7w5S7W4wwSgPwWhjZi9dC1kHB8Y6UYiaBaSQUbITiqQ/HkZ1LIzy12DqgQSndqCkM85EyFFYMOwCeKMTBGtdNJ7YtfwMZFUnFRZTbnyWSlK+NDUw2RNgFh6caHOIwmeW+rTC8oaXP5WwEJ9cWKJwSkcpCtSp3NdYKYiigs5WcGl9noP78cJinlKuR5TlqtTlo+1xKq2Z2Fkzncnr//E7MpFh7F4vl0xzHHhxfbAdYC6R3tHlYPss20riQn/ZOqo1UBQ/yQi2yE/UDhPjbtxPKOzvujGeuQrBQRxTaRxFz4uai6zBxNogpTYgRaByF0dCr59BhtRTcDx/GTrYOQwG6zgp0FrnArFR4IPhArEkpTWnFM7mwnT+ED+m9FaiC8JmyDKXToRWQEzSgjDlkbRNluQzoLx98z9C6etjmjbJ9a3x63+9td6ZRBIAAA==
```

***

## Importing Actions and Commands

Actions and Commands can be `Imported` from other installations of Streamer.bot (providing they have been created on an equal or earlier version), allowing you to share your creations to different PCs or even to entirely different streamers.

To Import an action, open the `Import` dialogue by pressing Import in the Top Left of Streamer.bot.

![importbutton.png](/importbutton.png)

You can Import 2 ways either paste in the UUEncoded string for the package you want or drag and drop a file with that contains your import code into the top box.

> If for some reason you are running streamer.bot with elevated permissions or in `Administrator` mode, you will be unable to use the drag-drop functionality, unless the Explorer window you are dragging from is also running in Administrator mode. 
To work around this you can temporarily load the application in regular mode while importing actions
{.is-danger}


Streamer.bot will attempt to recreate as best it can the action exactly as exported, though if it includes paths to files you will need to adjust these to match your folder structure before they will work.

The lower half of the window will then populate with a preview of all the actions found in that package.
You can select any of the actions you want to bring in, if any have an identical name to an action already in your library it will rename the incoming action(s)

> If you see no actions or commands populate when you copy and paste the code ensure that they are no trailing spaces or a new line at the end of the string. {.is-warning}

![importactions.png](/importactions.png)

The above example creates 2 Actions and 2 commands, you can use the checkmark to choose which Actions or Commands you wish to Import.