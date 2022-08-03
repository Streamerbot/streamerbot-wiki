---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2022-08-03T11:29:29.462Z
tags: 
editor: markdown
dateCreated: 2022-08-03T09:46:48.752Z
---

<font size="*3" class="mdi mdi-update text--twitch"><b> Changelogs</b></font>

---
# TwitchSpeaker v0.0.48
Released 2022-01-13{.subtitle}
* Fix mod/vip issue with non western characters
{.changelog-fixes}

<span></span>
* Added new option to change user said
{.changelog-new}

# TwitchSpeaker v0.0.47
Released 2021-12-25{.subtitle}
* settings/logs are moved to sub folders now, same as streamer bot
{.changelog-updates}

<span></span>
* Some additional error handling
* Added BadWordFilter setting for UDP Speak
* Added a new Generic Speaker form, that can be used to just play with the TTS, it was a request to be able to just use TTS
{.changelog-new}

# TwitchSpeaker v0.0.46
Released 2021-08-24{.subtitle}
* Fix speaking of first emote (was saying the last)
* Fix removal of emotes
* Fix BTTV emotes not being ignored if configured to
* Fix removal of cheermotes
* Fix minimum cheer amount not being used
* Fix speaking permission for subscribers
* Misc fixes/tweaks
{.changelog-fixes}

<span></span>
* Load channel rewards when connecting to Twitch
* Harden Twitch token validation
* Update TTS service libraries (AWS, Google, Azure, Watson)
* Improve shutdown time
* Update VIP/Mods when connecting to Twitch
* Update cheermotes to be case insensitive (cheer5, Cheer5 would both be caught now)
* Update networking code to support running on Linux
{.changelog-updates}

<span></span>
* Add option to be able to silence !tts command output
* Add Acapella TTS Service
* Add CereCloud Voice TTS Service
* Add new command (!tts permissions) to enable/disable specific permissions
* Add support for SevenTV emotes
{.changelog-new}

# TwitchSpeaker v0.0.45
Released 2021-08-24{.subtitle}
* Some fixes/changes
* Fix the Twitch host event, there were a few issues causing crashes
* Add %input% variable to Channel Reward messages
* Fix voice fall back selection, was not working correctly
* Misc fixes/improvements

# TwitchSpeaker v0.0.44
Released 2021-08-24{.subtitle}
* Enable and fix Twitch Host event
* Misc fixes/tweaks

# TwitchSpeaker v0.0.43
Released 2021-08-03{.subtitle}
* Add some error handling to UDP
* Misc fixes/tweaks

# TwitchSpeaker v0.0.42
Released 2021-07-22{.subtitle}
* Fix some issues with 3rd party emotes
* Better handling of Twitch API instabilities
* StreamElements fixes
* Twitch Authorization now forces the Authorize button so you can switch accounts.  Whenever you need to re-auth

# TwitchSpeaker v0.0.41
Released 2021-07-17{.subtitle}
* Fixes for StreamElements
* Added a new option to assign a voice; right click user, assign voice, dialog will popup where you can choose voice, assigning will auto-create alias and use it
* Only 1 instance of TTS can run now
* Small tweaks to UI
* Misc fixes/tweaks
* Other stuff I probably forgot

# TwitchSpeaker v0.0.40
Released 2021-06-20{.subtitle}
* Some fixes for streamlabs.com socket handling

# TwitchSpeaker v0.0.39
Released 2021-06-18{.subtitle}
* Make it a bit more friendly to those who aren't affiliate yet :)

# TwitchSpeaker v0.0.38
Released 2021-06-18{.subtitle}
* Fix BTTV/FFZ emote handling
* Fix Cheer event, seems I rushed this in the last version
* Fix for emotes not being completely removed (yay typos?)
* Add StreamElements support for Tips

# TwitchSpeaker v0.0.37
Released 2021-06-16{.subtitle}
* Fix ignore prefix, guess I overlooked something there

# TwitchSpeaker v0.0.36
Released 2021-06-16{.subtitle}
* Fix duplicate emote issue, yay?
* Guess it helps if the streamlabs token box is editable

# TwitchSpeaker v0.0.35
Released 2021-06-16{.subtitle}
* Updated twitch libraries
* Performance improvements
* Update handling of emotes
* When speaking everything, replies will be treated as normal messages
* When speaking everything, allow different prefixes to not speak anything
* Fix when saving audio files, if enabled
* Add auto reconnect to twitch
* !tts assign last `<user>` has returned
* Misc fixes and tweaks/cleanup
  
# TwitchSpeaker v0.0.34
Released 2021-05-12{.subtitle}
* Removed OneCore voices, this means there is no longer the hard requirement of windows, and may potentially work on Linux with Wine now
* Added a new cloud service, Microsoft Cognitive Services, this can add upto another 220 voices.
* Tweaked/fixed the cloud service voices use of pitch/rate/emphasis
* Fixes/tweaks to underlying twitch code

## IMPORTANT
I've altered the way the files are, so I would ## highly recommend extracing to a new folder and copying your settings over. (settings.json, voicealiases.dat, users.dat, usage.dat)

## IMPORTANT

## Some updates to Pitch/Rate/Emphasis

## Amazon Poly
Rate can now be adjusted from `-20` to `20`, this equates to a 5% change in rate from baseline, pitch can now be adjusted from `-9` to `11`, this is a 5% relative change from baseline. Pitch is ## NOT supported on Neural voices Emphasis is supported on Standard voices only.

## Google Voice
Rate can now be adjusted from `-20` to `20`, this equates to a 5% change in rate from baseline; Pitch can now be adjusted from `-19` to `21`, this is a 5% relative change from baseline. Emphasis is supported on Standard and WaveNet voices.

## IBM Watson
Rate can now be adjusted from `-20` to `20`, this equates to a 5% change in rate from baseline; Pitch can now be adjusted from `-19` to `21`, this is a 5% relative change from baseline. Emphasis is ## NOT supported on any voices.

## NOTE In testing, I found the Watson voices to behave a bit strange when going to the extremes

## Microsoft Azure
Rate can now be adjusted from `-10` to `10`, this equates to a 5% change in rate from baseline; Pitch can now be adjusted from `-9` to `11`, this is a 5% relative change from baseline. Emphasis is supported on Standard and Neural voices (might be hit or miss on neural voices).

# TwitchSpeaker v0.0.33
Released 2021-05-04{.subtitle}
* Added some more logging
* Fixed audio device selection, guess I missed something with that
* Updated HypeTrain end event for future possibilities

# TwitchSpeaker v0.0.32
Released 2021-05-01{.subtitle}
* Fix issue w/ twitch library and cancelling raids
* Fix issue when setting certain options via twitch chat
* Add ability to use !tts commands via whisper, these will provide no feedback, and can be enabled/disabled via a setting
* Added auto backup capability, on application start, it will auto zip up your config files into a time stamped zip file within a backups folder

# TwitchSpeaker v0.0.31
Released 2021-05-01{.subtitle}
* Fix a potential crash with subs, seems twitch changed data (yay)
* No longer listen to sub events via pubsub, was pointless, they're obtained by other means

# TwitchSpeaker v0.0.30
Released 2021-04-25{.subtitle}
* Fixed issue with buffers, so, it shouldn't repeat itself anymore

# TwitchSpeaker v0.0.29
Released 2021-04-24{.subtitle}
* Fixed issue with buffers, so, it shouldn't repeat itself anymore

# TwitchSpeaker v0.0.28
Released 2021-04-19{.subtitle}
* Add days left to the Community goal contribution event, use %daysLeft% to get this value
* Add new !tts set nickname `<username>` `<nickname>` to allow a mod to set a users nickname, setting it to nothing will remove the nickname
* Fix text replacement UI, ctrl*up/down wasn't behaving properly to change ordering
* Minor fixes/tweaks
* Updated twitch authorization mechanisms, it may re-ask for authorization, will also no longer complain constantly if there's an issue with your login and allow you to re-auth properly

# TwitchSpeaker v0.0.27
Released 2021-04-11{.subtitle}
* Squahsed a bug

# TwitchSpeaker v0.0.26
Released 2021-04-11{.subtitle}
* Misc fixes/cleanup
* Twitch chat client is running on a new parser, small speed improvements
* Better audio device enumeration (you'll see disconnected devices now to)
* Added Voice Aliases
* Addde ability for deleting a users message, timing a user out and banning a user to stop/skip speech (enabled by default)
* Fix a bug where using stop would hang the application

# TwitchSpeaker v0.0.25
Released 2021-03-26{.subtitle}
* Fix Twitch FUCK UP
* Misc tweaks/fixes

# TwitchSpeaker v0.0.24
Released 2021-03-14{.subtitle}
* Fix audio device not being selected on startup (woops)
* Toggling enabled caused a crash, fixed, but not sure why, need to investigate
* Fix small issue w/ UDP

# TwitchSpeaker v0.0.23
Released 2021-03-14{.subtitle}
* Handle regex errors gracefully, and provide feedback when entering regex in replacement

# TwitchSpeaker v0.0.22
Released 2021-03-13{.subtitle}
* Clicking on edit voice will bring speech preview in focus, and enable the next feature
* Ability to assign a voice right from the speech preview window.
* Add grace period (in seconds) for saying username
* Fix community goal % contribution, I think?
* Handle some google voice statup exceptions, this is still ongoing
* Add option to say username only if the previous message was from a different user, can't be used with the grace period
* Channel Rewards can now have random weighted messages, like events
* Added new randomization code, will see how it works
* Add option to swap name with nickname if one is set for a user
* Misc cleanup and bug fixes
* Add a UDP listener, will outline the commands later
* Add ignored voice profiles
* Add regex replacement, don't make me regret this.
* Re-organize settings tab

## Ignored Voice Profiles
You can now setup profiles for ignored voices/locales.

This adds a new moderator command !tts profile, !tts profile list, !tts profile activate

## Regex Replacement
I know a lot have wanted this feature, and I've been very reluctant on adding it. Flat out, if I get wind of it being used in a purposefully hateful/hurtful way, I will pull all zips that have this version, and remove the code for it.

This replacement will occur for ## all spoken text (message, events, etc), in the chain of events, this is the last thing processed.

An example replacement: Replace: `[_\-!@#$%^&*()]*,` With: a space, this will replace 1 or more, of any of the characters with a space, so a username that has _ in it, will get spaces instead. Replace: `\d{3,}`, With nothing, this will remove all occurances of 3 or more numbers

Order of replacements is also something to keep in mind

# TwitchSpeaker v0.0.21
Released 2021-02-20{.subtitle}
* Harden some Twitch API calls to hopefully not cause as many crashes, this is an on-going thing
* Add a check to prevent follow spam, during a session (open/close of program) a follow will only be fired once for a user and any further ones will be ignored
* Misc fixes/tweaks

# TwitchSpeaker v0.0.20
Released 2021-01-06{.subtitle}
* Audio output is now using WASAPI instead of WaveOut for, reasons.
* Added new option to select the audio output device, this effects all speech; may expand this to be more granular, not sure yet.  Option is on TTS Settings page
* Some misc fixes/tweaks
- NOTE: Only WASAPI supported output devices will be listed.
- And yes, I know, the UI is still fugly, it's on my ever growing list.

# TwitchSpeaker v0.0.19
Released 2020-10-02{.subtitle}
- Full on 4s, thought I'd give them back now.

# TwitchSpeaker v0.0.18
Released 2020-10-02{.subtitle}
* Fix !tts assign last `<user>`, it should now actually work
* Fix random sticky voice option, it should also now work
* Add community goal contribution and finished events to events that can be spoken.

Default event strings for contribution is: `Well, %name% decided to contribute %amount% towards %title%, it's %percent% finished, getting closer!`

Default event string for goal finished is: `Amazing, %title% was just finished, %amount% points were used to fund it!`

These will not be added to existing settings, so be sure to configure them if you would like to use them.
# TwitchSpeaker v0.0.17 (date unknown)

# TwitchSpeaker v0.0.16
Released 2020-09-22{.subtitle}
* Small fix to the delayed text save

# TwitchSpeaker v0.0.15
Released 2020-09-22{.subtitle}
* Misc fixes
* UI cleanup a bit, finally switched scaling in VS, so controls shouldn't overlap/etc anymore
* Fix text input dialog focus
* Ability to edit the nickname of a user directly, this is tested as best I can, it should be ok, its a delayed saving
* Umm stuff I probably forgot?

# TwitchSpeaker v0.0.14
Released 2020-09-05{.subtitle}
* Misc bug fixes

# TwitchSpeaker v0.0.13 (date unknown)

# TwitchSpeaker v0.0.12
Released 2020-08-08{.subtitle}
* Deadlock resolved, I think
* Watson is now auto enabled if configured to
* AWS Keys are masked
* Toys were put away for now
* Implement some checks on settings files so they're not wiped
* Error handling for engine inits, hopefully it won't crash now when aws/google/watson has issues on initial setup
* Auto connecting option added
* Other misc fixes/bugs

# TwitchSpeaker v0.0.11
Released 2020-08-01{.subtitle}
* New TTS Engine! IBM Watson, adds another 50 voices, with default install of windows and all engines active, you now have 376 voices
* Separate ignore emote setting into the 3 services (Twitch, BTTV, FFZ), be default, BTTV and FFZ are not ignored, so be sure to toggle those to return to default behaviour
* Misc fixes here and there
* Update viewer display names when possible
* Start tracking character counts, for now this is just put to a file, there will be a display area somewhere eventually
* New Gag button to outright silence TTS
* Other stuff I can't remember at the moment

# TwitchSpeaker v0.0.10
Released 2020-07-10{.subtitle}
* Fix crash Thelete reported
* Update some default strings
* Add subscription related info back in, this requires a new scope, so you'll need to re-auth, app will inform you
* Misc fixes/tweaks

# TwitchSpeaker v0.0.9
Released 2020-07-07{.subtitle}
* Bump SAPI5 sampling rate

# TwitchSpeaker v0.0.8
Released 2020-07-07{.subtitle}
* Forgot to add the ability to force a user's speech, so, you can now force a user to always have there chat spoken, maybe tweaked a bit still (i.e. you could force a user, and disable all permissions, and their text would still be spoken)

# TwitchSpeaker v0.0.7
Released 2020-07-07{.subtitle}
* Not allowed response being to aggressive, gave it a stern talking to
* Added !tts reg [add|del] [username] to add/remove regular status of user
* Events Settings: Forgot to clear Enabled check box in the message area when picking another event type
* Ignore exclimation was also being to aggressive, gave it a stern talking to as well

# TwitchSpeaker v0.0.6
Released 2020-07-06{.subtitle}
* Fix an issue w/ gift sub event strings not saying the tier
* Add ability to disable an event string, so you don't have to delete it to not use it
* Fix removing an ignored voice (on TTS Settings tag)
* Misc tweaks/fixes

# TwitchSpeaker v0.0.5
Released 2020-07-06{.subtitle}
* Will actually ignore a user now if flagged as ignored
* Misc fixes/tweaks

# TwitchSpeaker v0.0.4
Released 2020-07-06{.subtitle}
* Fix not being able to connect after disconnect
* Fix everyone permission
* Few misc fixes/tweaks