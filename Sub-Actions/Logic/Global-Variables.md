---
title: Global Variables
description: 
published: true
date: 2022-06-28T00:49:19.141Z
tags: 
editor: markdown
dateCreated: 2022-06-28T00:49:15.047Z
---

# Global (Get)

![logic-global-get.png](/logic-global-get.png)

This sub-action copies data from a stored `Global` type variable into a custom `Argument` so it is available to the rest of the action.

## Source

Global variables can be stored with or without an associated `userID`
`Global` source are single variables that have the same data no matter the user context

`User` source stores a copy of that variable name against each unique user so when data is retrieved it will pull based on the selected context:

User Context | Description
-----|-----
`Redeemer`|Pull the information for the user activating the action
`Target`|Pull the information for the current `targetUser` - Used in conjunction with the [Get Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target) sub-action


## Persisted

Any Global / User variable can be set as `Persisted`. If this flag is set Streamer.bot will save the data into the `Globals.dat` file in the `Data` folder. Data saved in this way will survive application restarts. 
When fetching data you can select to use the persisted data store or the temporary one. 
> These data stores are completely separate so data stored in the `Persisted` memory will not be copied to the `Temporary`. Generally speaking you will always want to match your data store
{.is-warning}

## Variable Name

This is the name of the `Global` / `User` variable to fetch
> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

## Destination Variable

This is the name of the custom `Argument` the data will be stored in.
> It is best practice to always name this something different than the `Global` you are reading from. Not only does this make your workflow easier to read and debug, it can also prevent strange issues with logic and inline functions
{.is-success}

## Default Value

If the specified `Global` / `User` variable does not exist for that context, the Get subaction will create it for you and populate with this value

***

# Global (Set)

![logic-global-set.png](/logic-global-set.png)

## Destination

This sub-action stores data in one of the `Global` data stores, valid options are `Global` & `User`
`User` context is further subdivided into `Redeemer` & `Target`

User Context | Description
-----|-----
`Redeemer`| Store data for the user activating the action
`Target`| Store data for the current `targetUser` - Used in conjunction with the [Get Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target) sub-action

## Persisted

Data can be stored in a `Temporary` store or a `Persisted` store. Persisted data will be saved to the `Globals.dat` file in the `Data` folder. Data saved in this way will survive application restarts. 

## Variable Name

This is the name of the `Global` / `User` variable to write to
> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

## Content

The final line provides space to define what to store in the named `Global`
This has 3 modes:

Mode | Description
-----|-----
`Value`| Store the entered value, exactly as written 
`Increment`| Take the current global vlaue and add the specififed value to it (only works for intergers)
`Argument` | Store the contents of a named active argument (do not include the % symbols)