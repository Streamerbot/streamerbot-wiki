---
title: Logic Sub-Actions
description: Sub-Actions Reference
published: true
date: 2022-10-06T23:54:41.965Z
tags: subactions, logic, if, else, set argument, break, global variables
editor: markdown
dateCreated: 2022-06-28T00:50:33.068Z
---

Complex actions can be built using the logic operators in Streamer.bot. 

These will take data from various sources and evalutate them to direct the action, so understanding how they interact is key to building the workflow you want.

All logic in Streamer.bot must be performed against active Arguments. As any argument can only persist until the end of the running action if data need to be saved between actions, Global Variables can be used. Their data must be copied into an Argument to be usable

> Global Variables should always be stored in `camelCase` ie. with a lower case initial letter.
> Streamer.bot can not retrieve data from any store if the initial letter is capitalised.
{.is-danger}

> It is best practice to always name your `Arguments` something different than the `Global` you are reading from. 
> This will make your workflow easier to read and debug and can also prevent strange issues with logic and inline functions
{.is-warning}

* [**Global (Get) *Read data from a`Global Variable` into an argument***](/en/Sub-Actions/Logic/Global-Variables#global-get)
* [**Global (Set) *Save data to a custom `Global Variable`***](/en/Sub-Actions/Logic/Global-Variables#global-set)
* [**If / Else *Performs an `Action` if logical test is `True`***](/en/Sub-Actions/Logic/If-Else)
* [**Set Argument *Store / Manipulate data in an argument***](/Sub-Actions/Logic/Set-Argument)
* [**Break *Diagnostic user only, cancels the running action***](/Sub-Actions/Logic/Break)
{.btn-grid .my-5}


## Variable Types

Streamer.bot has 2 main variable types; `Global` and `Argument`

`Arguments` will only persist until the end of the currently executing action (or any Action called by it)
Sub-actions in the UI can only use `Arguments` as a data source

> C# can access an Action's active Arguments using the `args` directory 
{.is-info}

***

`Globals` will persist beyond the end of the action and are generally used to store data that needs to be read by future Actions

Thier data can not be used directly in an Action. To use them a `Global (Get)` sub-action must be added to copy the currently stored data into a temporary argument. Subsequent sub-actions can then use this argument and data can be written back to Global storage using a `Global (Set)` sub-action.


## Global (Get)

![logic-global-get.png](/logic-global-get.png)

This sub-action copies data from a stored `Global` type variable into a custom `Argument` so it is available to the rest of the action.

### Source

Global variables can be stored with or without an associated `userID`
`Global` source are single variables that have the same data no matter the user context

`User` source stores a copy of that variable name against each unique user so when data is retrieved it will pull based on the selected context:

User Context | Description
-----|-----
`Redeemer`|Pull the information for the user activating the action
`Target`|Pull the information for the current `targetUser` - Used in conjunction with the [Get Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target) sub-action


### Persisted

Any Global / User variable can be set as `Persisted`. If this flag is set Streamer.bot will save the data into the `Globals.dat` file in the `Data` folder. Data saved in this way will survive application restarts. 
When fetching data you can select to use the persisted data store or the temporary one. 
> These data stores are completely separate so data stored in the `Persisted` memory will not be copied to the `Temporary`. Generally speaking you will always want to match your data store
{.is-warning}

### Variable Name

This is the name of the `Global` / `User` variable to fetch
> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

### Destination Variable

This is the name of the custom `Argument` the data will be stored in.
> It is best practice to always name this something different than the `Global` you are reading from. Not only does this make your workflow easier to read and debug, it can also prevent strange issues with logic and inline functions
{.is-success}

### Default Value

If the specified `Global` / `User` variable does not exist for that context, the Get subaction will create it for you and populate with this value

***

## Global (Set)

![logic-global-set.png](/logic-global-set.png)

### Destination

This sub-action stores data in one of the `Global` data stores, valid options are `Global` & `User`
`User` context is further subdivided into `Redeemer` & `Target`

User Context | Description
-----|-----
`Redeemer`| Store data for the user activating the action
`Target`| Store data for the current `targetUser` - Used in conjunction with the [Get Info for Target](/en/Sub-Actions/Twitch/Get-User-Info-for-Target) sub-action

### Persisted

Data can be stored in a `Temporary` store or a `Persisted` store. Persisted data will be saved to the `Globals.dat` file in the `Data` folder. Data saved in this way will survive application restarts. 

### Variable Name

This is the name of the `Global` / `User` variable to write to
> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

### Content

The final line provides space to define what to store in the named `Global`
This has 3 modes:

Mode | Description
-----|-----
`Value`| Store the entered value, exactly as written 
`Increment`| Take the current global vlaue and add the specififed value to it (only works for intergers)
`Argument` | Store the contents of a named active argument (do not include the % symbols)

***

## If Logic

![logic-if.png](/logic-if.png)

The If sub-action performs a logical test on the contents of an `Argument` and if the result is true it will perform a named action and then either break the action or let it continue

> If the test comes back `False` the rest of the IF statement will be ignored and the action will always continue to the next sub-action 
{.is-warning}

### Variable

This is the `Argument` name to test

> If you are still using v0.14 or belowm do not use % symbols in the variable name, for v0.15 and up it % symbols will be ignored in the Variable name
{.is-info}

### Operator

The Type of logical test to perform. Valid options are `Equals`, `Not Equals`, `Contains`, `Regex Match`, `Less Than`, `Greater Than` & `Does Not Exist`

### Value

The value for comparison 

### Do Action

The `Action` to perform if the logic test is true

If the `Run Action Immediately` checkbox is ticked, this will run the action outside of its normal queue as if it were a subroutine of the current action, Streamerbot will return to this point in the action after it has completed

If the box is unchecked then Streamerbot will queue it as normal as a completely separate action and then move on immediately to the next sub-action

### Then

This specifies if the Action should `Continue` or `Break` after performing its named Action. This flag will only trigger if the test was `True`, if not it will always `Continue`

***

## Set Argument

![logic-set-argument.png](/logic-set-argument.png)

This sub-action is used to define custom `Arguments` or perform [Inline Functions](/en/Inline-Functions) with them such as [Math](/en/inline-functions-math)

### Variable Name

The `Argument` you wish to manipulate (This should be without the % symbols)

### Value

The data you want to store in the argument

***

## Break

This is a diagnostic Sub-action that will cancel execution of the action

---

- [<i class="mdi mdi-chevron-left"></i>**Sub-Actions Reference *Go Back***](/en/Sub-Actions)
- [<i class="mdi mdi-network primary--text"></i> **Network *Sub-actions reference for network requests***](/en/Sub-Actions/Network)
{.btn-grid .my-5}
