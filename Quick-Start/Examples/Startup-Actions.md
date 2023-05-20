---
title: Quick Start -  Startup Actions
description: 
published: true
date: 2022-09-19T07:12:57.792Z
tags: 
editor: markdown
dateCreated: 2022-09-19T07:11:54.085Z
---

## Import Code
```text
TlM0RR+LCAAAAAAABACtVVtvokAUft9k/4PhuZjhJtKkDxZbq03doPVSlz4MMwNlO1yWi2ib/vedgboi2k2bLInKnG/mO9/58Bxev39rtYQ1SVI/CoXzlnRWBkIYELYShGoJUcbglEV+8nWr9Vr9MMjHfB8wdFV3kSaqqIvYl6aJ0FAMUVF1Te9ghLpQq7jKQ79zknP+MKd0HyUhdCjhfFmSk318J2Z6KQ5DP6vxeEmUx3udZQzSAm7TSc6rcSFNa0QJDHEU9MpijlEUhShPEhJmx9iRAQcm/FtliWKSosSP3zMLDfSZkLhH/TVp1l7JJi5hshBp5C9B89y2C5/VVaS2feejJEojN2uPr+5t+zphmoooee6otr1W26CtAEUybDtIUZRQ32ljSoU64eNhZmebETPCZV14OY6dAHkzhb7gwTz7UYDbvhUXeDFK4eLOe5A3T0i58yzpcjhdaCymUYbrfSsa8Q+6mfvOgP4a3qzWcGF5bE+MTS/mGGFcpkX7sysvn4Xz3FqMAVwY+a05urd8aeQEFAz9wlsF1ymSZzHPbS7B2PTAbZN3MqAvaGC8rKYH3NvVciKhQC31uBbXXtM0GK0dufAmyyf6oMxB46z8sBx6xOwZw36vPG8uRxTfzLeOfwlQOKd/9YRc08VF4/HGCUFREPv09PPFhMLtNINJdhKuOgypiuQ6UBdBR2IdpjlYdCQdi8RwsKroqtrVO420BfG9J84J2uAQybYxl2Lw6xDZddRBZ5bIB91ZSQwx2fBE++jb2UeNkpENFyWkTivlRTPOI7vYHz4huIdQlJftCE5Zgh0XQo1NGaJDV1Q7GItQxUBEBMqyJiMFaPCrlkjgf/ohf8aPNaR5lZpdhzwB3Mzf0QZSjbKjQVVzB7qAzV2oiTomqqhiQxK7imwwd/SuYsiygzTp6+4A+bQ/zYn2GXekmju728fmzB3wBOXge6yPakphnBJcQyuwJKp2Vm+ZHfj2B/c4W63qBgAA
```

## Installation
In Streamer.bot in select `Import` from the top left.
Copy the `Import Code` and paste it into the `Import String`. 

## Configuration
In the `Action` it waits 10 sec to give SB time to connect to twitch and then send a "streamerbot connected" message.
The only important part is the name of the `Action` being `"SB-Init"` and the code `Subaction` which should **NOT** be changed...
The rest of the `Action` can be adapted to anything you want done right after SB starts.

>Right after means right after queues are initialized...you may have to wait for the features you want to be actually loaded (like the Twitch connection).
{.is-info}
---

- [<i class="mdi mdi-chevron-left"></i> **Quick Start Guide *Go Back***](/en/Quick-Start)
- [<i class="mdi mdi-twitch text--twitch"></i>Made by Krayn](https://www.twitch.tv/Krayn_)
{.btn-grid .my-5}