---
title: SetFilenameFormatting
description: Enable/disable sending of the Heartbeat event
published: true
date: 2022-06-29T17:58:28.934Z
tags: 
editor: markdown
dateCreated: 2022-06-29T17:58:28.934Z
---

# SetFilenameFormatting

## Example
```json
{
"request-type": "SetFilenameFormatting",
"filename-formatting": "%CCYY-%MM-%DD %hh-%mm-%ss"
}
```
## Request Fields
| Name | Type | Description |
|-----:|:----:|:------------|
| `filename-formatting` | <kbd>string</kbd> | Filename formatting string to set.

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
| `obsRaw.status` | <kbd>string</kbd> | The status of the OBS raw sub-action
| `obsEvent._json` | <kbd>string</kbd> | Everything above in a json format
## Explaination
> Details coming soon...
{.is-info}

## Import

```
TlM0RR+LCAAAAAAABACVU8tOwzAQvCPxD1akSCBhlOZBW2481MKhQqJcEOHgJJs2kuMUP2irqv+OHTciTcoBH5J4d2Z3PZ7szs8Qcr6Bi6Jizi3yr+oAIyXonfNyP0ecrBFGU2DACUUXc5CTgoJBTCpeEikLtrh0LI+kUtcRmvph9gjt7EuniswUjJIgAD9KsJdEYxzmIWASmO0gTJPhELLU92ytmvSlQJlBmKL0N6qbJxRMPckVtOKblKoMJrwqnwohK77VkJxQ0cI0Jzt5jFbnBa/U6qQELRCha7IVr4r1+3DCsqq8q/XoZ9OKpYpzYLKf62l4pON/DlFjVxzyYtPV8DDj2lTZxTxmscNBqy0kltsVxDoeny4fO1cWnx9SOG/lDM19eHh/x+5sht3HR+Qul9gtS+wKETuGue8MyEEoKsVbdccXonunjVoMalWeaxN5h4VPPJrVaWLdN8qCUZiQCEfDMMNhNLrB4zwieJyAPxiTgJDA7xDXUCyW5pa8a+84Y3TS8fDmONwYpy/3H7a187EMzCV5v9F98/nZ9cbUtKgN8tm2FKVkJSBrZW2yLmSR9odqUTWtLLVVG/z+B7ZU8K8RBAAA
```