---
title: Arrays
description: 
published: true
date: 2022-07-19T13:45:29.204Z
tags: 
editor: markdown
dateCreated: 2022-07-17T14:26:01.568Z
---

<h1 class="mdi mdi-code-array primary--text"> JSON Arrays</h1>

> More info to be added soon...
{.is-info}
## Looks
### Example 1
Here you see 3 nested objects inside of this array{.subtitle}


### Tab {.tabset}
#### Normal
```json
[{"name":"nested object"}, {"name":"nested object"}, {"name":"nested object"}]
```
#### Other
```json
[
  {
    "name":"nested object"
  }, 
  {
    "name":"nested object"
  }, 
  {
    "name":"nested object"
  }
]
```

### Example 2
Here you see an array with 3 integers{.subtitle}
### Tab {.tabset}
#### Normal
```json
[10, 20, 30]
```
#### Other
```json
[
  10, 20, 30
]
```
### Example 3
Here you see an array with a nested object and a nested array with 3 integers, 1 boolean and 1 string{.subtitle}
### Tab {.tabset}
#### Normal
```json
[{"name":"nested object"},[10, 20, 30, false, "nested array"]]
```
#### Other
```json
[
  {
    "name":"nested object"
  },
  [
    10, 20, 30, false, "nested array"
  ]
]
```
## Explanation
A JSON array contains elements separated by comma's, The JSON array is surrounded by square brackets <span class="mdi mdi-code-array primary--text"></span>.

### Break Down

Elements: An element is something from this list of <span class="mdi mdi-sprinkler-variant primary--text"> Data Types</span> below

- [<i class="mdi mdi-sprinkler-variant primary--text"></i> **Data Types *Information about all kind of Data Types used in coding e.g. string, integer, object***](/en/Sub-Actions/Code/Data-Types)
{.btn-grid .my-5}