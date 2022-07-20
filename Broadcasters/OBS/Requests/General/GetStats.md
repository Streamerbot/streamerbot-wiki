---
title: GetStats
description: Get OBS stats (almost the same info as provided in OBS' stats window)
published: true
date: 2022-07-03T21:05:13.037Z
tags: 
editor: markdown
dateCreated: 2022-06-29T18:29:33.547Z
---

# GetStats

## Example
```json
{
"request-type": "GetStats"
}
```

## Request Fields
> No request fields required.
{.is-success}

## Variables
| Variable | Type | Description |
|---------:|:----:|:------------|
| `obsRaw.stats.average-frame-time` | *double*{.datatype} | Average frame render time (in milliseconds)
| `obsRaw.stats.cpu-usage` | *double*{.datatype} | Current CPU usage (percentage)
| `obsRaw.stats.fps` | *double*{.datatype} | Current framerate
| `obsRaw.stats.free-disk-space` | *double*{.datatype} | Free recording disk space (in megabytes)
| `obsRaw.stats.memory-usage` | *double*{.datatype} | Current RAM usage (in megabytes)
| `obsRaw.stats.output-skipped-frames` | *integer*{.datatype} | Number of frames skipped due to encoding lag
| `obsRaw.stats.output-total-frames` | *integer*{.datatype} | Number of frames outputted
| `obsRaw.stats.render-missed-frames` | *integer*{.datatype} | Number of frames missed due to rendering lag 
| `obsRaw.stats.render-total-frames` | *integer*{.datatype} | Number of frames rendered
| `obsRaw.status` | *string*{.datatype} | The status of the OBS raw sub-action
| `obsEvent._json` | *string*{.datatype} | Everything above in a json format

## Explaination
> Details coming soon...
{.is-info}

## Import
```
TlM0RR+LCAAAAAAABACFUs9PgzAUvpv4PzScNLGmsI4Fb/Pg9GTivMkOBd4mSSnYH7Jl2f9uC8MxmLEHaL/3vV/fe/vrK4S8b5AqL4X3gIK7BhCsAPvyXh+XSLIaYbQAAZJxdLMAvdRMq1uvpbJUW1dl2R/ujdC+/VlTnrkYSbYmlBGCAxJGmPphgiMaTXAASUBTkiSzKGpjNU5fBozLLQznJxQESzi4eFoa6OHblJsMnmRZPOdKl3JnKWvGVY/TNdNV3ku2kaWpLjbaIzFes516M2IcWjKRlcW8kWBsTUuRGilB6LFtJNuZdP/U3ZgrCet8O1TqWFbtHPexjEXsSbCaKo31roLY4vFvxNhzjMMgsARluFbv5Vxu1FDxrjEBTQMvzYjJ8eALn+4MkrS7QSPqUxqmeDr1we4GAE4YiXAwCydkCpkf+sHAsYZ88+kEJffk3OL6szgNz+FuxmOZ/liqtj6RgROXnNBDd10Nx7hwKZpZrvrT55xVCrKetTU2gVpmu+49V+tWFHarOv7hB4Dvud+iAwAA
```