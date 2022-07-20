---
title: SetHeartbeat
description: Enable/disable sending of the Heartbeat event
published: true
date: 2022-07-03T21:06:01.253Z
tags: 
editor: markdown
dateCreated: 2022-06-29T17:50:09.657Z
---

# SetHeartbeat

## Example
```json
{
"request-type": "SetHeartbeat",
"enable": "True"
}
```

## Request Fields
| Name | Type | Description |
|-----:|:----:|:------------|
| `enable` | *boolean*{.datatype} | Starts/Stops emitting heartbeat messages

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
| `obsRaw.enable` | *boolean*{.datatype} | Indicates whether authentication is required.
| `obsRaw.status` | *string*{.datatype} | The status of the OBS raw sub-action
| `obsEvent._json` | *string*{.datatype} | Everything above in a json format
## Explaination
> Details coming soon...
{.is-info}

## Import
```
TlM0RR+LCAAAAAAABACNU0tPhDAQvpv4HxpOmliDpOyy3vTg42Si3sTDQIeVpJS1D9fNZv+7LV2yLGhiD0C/+eb1zbA9PSEk+kKl61ZG1yS56AAJDbpb9HT7QhSsCSX3KFGBIGcvaB4QlCkQzHkU6FAa566dx5u/E7INL2equY9TpQsWsyqjWZkyyuIko8W84DSdxUVZQcwXrAqxOqdPi9bnl1aIA4oSCoE+nlEWB/h3KSzHO9U2D7U2rdo4SgVCDzh9Q8PqBwmXqrWrXxsekECsYaOfrZyGVyB529x0MkytZStLqxRKM7VNpDuS7x+1d5SVwqr+Hiu2L23tnbe5ymUeKXTaakPNZoW5w/OjqHl0EWhB6kB4dWLnkcd3o6wKtRVGv7Y3aqnHY+k7l9h1+NjtQbw/9JdHf0ZJ9guUVNmC8RlNWbKgDNKCwiyZU54wuLqCbF6mychxjfXywyseX8bHFt+8w9nsGO6XYKrhH5sX6pMcvfLxAd31n+/jOd/7FN2w34frIQSsNPKBNRi7QIEZ/omBq3NrGrd2PX/3A1SEs1zLAwAA
```