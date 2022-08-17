---
title: Perform Command
description: Sub-Actions Reference
published: true
date: 2022-08-17T16:19:32.167Z
tags: subactions
editor: markdown
dateCreated: 2021-08-25T21:33:38.438Z
---

## Overview

With this sub-action, you can run an exe, batch file, cmdlet, Powershell script, URI, or anything you can normally run via the <kbd>Win+R</kbd>, Windows Run dialog, or command prompt.

A common usage for this action, is using the LIV URI for switching camera profiles `liv-app://camera/set/#`

![perform-command-dialog.png](/Sub-Actions/perform-command-dialog.png =300x)

## Configuration

### Command
The command or executable to run

### Working Directory
The working directory for the command - defaults to the directory of the executable

### Arguments
Optional arguments or flags to pass to the executable

### Wait
Optional delay in seconds

### Environment Variables
Define any optional environment variables you would like to pass to the executable

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/en/Sub-Actions)  
- [<i class="mdi mdi-network primary--text"></i>**Network *Fetch URL, UDP Broadcast***](/en/Sub-Actions/Network)
{.btn-grid .my-5}