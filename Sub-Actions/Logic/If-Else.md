---
title: If/Else
description: Working with variables and logic statements
published: true
date: 2022-10-19T06:00:32.161Z
tags: logic, if, else
editor: markdown
dateCreated: 2022-01-09T11:33:31.443Z
---

## Overview

![logic-if.png](/logic-if.png)

The If sub-action performs a logical test on the contents of an `Argument` and if the result is true it will perform a named action and then either break the action or let it continue

> If the test comes back `False` the rest of the IF statement will be ignored and the action will always continue to the next sub-action 
{.is-warning}

## Variable

This is the `Argument` name to test

> If you are still using v0.14 or belowm do not use % symbols in the variable name, for v0.15 and up it % symbols will be ignored in the Variable name
{.is-info}

## Operator

The Type of logical test to perform. Valid options are `Equals`, `Not Equals`, `Contains`, `Regex Match`, `Less Than`, `Greater Than` & `Does Not Exist`

## Value

The value for comparison 

## Do Action

The `Action` to perform if the logic test is true

If the `Run Action Immediately` checkbox is ticked, this will run the action outside of its normal queue as if it were a subroutine of the current action, Streamerbot will return to this point in the action after it has completed

If the box is unchecked then Streamerbot will queue it as normal as a completely separate action and then move on immediately to the next sub-action

## Then

This specifies if the Action should `Continue` or `Break` after performing its named Action. This flag will only trigger if the test was `True`, if not it will always `Continue`

---

- [<i class="mdi mdi-chevron-left"></i> **Logic Sub-Actions *Go Back***](/en/Sub-Actions/Logic)
{.btn-grid .my-5}