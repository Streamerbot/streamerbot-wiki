---
title: MIDI
description: Musical Instrument Digital Interface
published: true
date: 2023-01-19T19:48:23.987Z
tags: v0.1.15, midi
editor: markdown
dateCreated: 2022-11-24T09:49:55.140Z
---

## MIDI In
It's now be possible to run actions by using your MIDI Piano, and MIDI synth, oh, even your MIDI wind instrument, or anything that supports MIDI!

When adding an `Event`, you will be able to just press the key, turn the knob, or flick the wheel to have it auto populate all the settings for you.

This section is a WIP for information, but to get you started, here are some screenshots.

![midi-04.png](/midi/midi-04.png)

Add a new MIDI In device
![midi-01.png](/midi/midi-01.png)

Add a new MIDI event
![midi-03.png](/midi/midi-03.png)

Editing a MIDI event
![midi-02.png](/midi/midi-02.png)

To get started with MIDI follow these steps:

1. Add a Device, to do this, right click in the top section of the MIDI tab, and click Add
2. Pick your device from the drop down, and give it a name, and click Ok
3. Select the device you just added
4. Right click anywhere in the bottom list, and Add an event.
5. With the Add Event dialog open, you can press any of the keys on your device to have it fill in all the data for you and show an example of what the arguments will look like.

## MIDI Out
The other side of MIDI, being able to send MIDI events out to your devices or DAWs.

Much like MIDI In, you create a device mapping within Streamer.bot, and you can use 1 of 3 new sub-actions to send MIDI events.