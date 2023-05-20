---
title: Log All Arguments Example
description: 
published: true
date: 2023-04-07T20:41:17.989Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:31:42.148Z
---

Here is an example that will log all the arguments that you have access to for an action.  It's best to add this as is, and then use the [Execute C# Method](/Sub-Actions/Code/CSharp/Execute-Method) to use it in your other actions.

# Tabs {.tabset}
## Code
```csharp
using System;

public class CPHInline
{
    public bool Execute()
    {
        foreach (var arg in args)
        {
            CPH.LogInfo($"LogVars :: {arg.Key} = {arg.Value}");
        }

        return true;
    }
}
```

## Import String 
```
TlM0RR+LCAAAAAAABAB1U11zojAUfe9M/4Pj8+LwqdKZPiitiFZdaosfSx9CEpA1EDaAlu30v28AW6t2mQnh3nNzzrlD7tv1VaPR3GGWhjRu3jSkH1UiBhHmUfOBBg5gabPOApjxqpQDv8q40XirNw6FqCzXFR/rbUkWVEnlL7kLhW5Hl4WuCiSpo8maCkDNVR36k+O8lIlzQo7Zb7UrhIEY0ahXueAVPiApPqKQxjBnDMfZJXbh/MT9iexRr0ojnEIWJgfJc3SLcdIj4Q5fSNaGsY+5IYjPlCvQuHHdRcg72qeuOwkhoyn1s9b0/sl1B4y72VO2dd2d2hJbiqhIuutGKaSMhF4LEdL8SvdyqusVGTYoqvpBy2niRTB4VshfZDrZbC+O7+xkjxajFCwmwUp+3UBlEthS35ovNJ7TCMc7dzYNLKMXwKETeib5bZmjnSfvg8flhqwUR1zPg+SjBnPOcq9XP/KUEVktptQyNvJqaQWr5Si2TJJb5qBYK5PPc9UaplMj7B3jct1P7bmhTTwZjbxovRsbdvhk6rETDQpY9NqzsN8pOR+2GcFLMfg5P8RkvfGGDvHnVjI79aRzzRMdGDkiWo5ya/hYoMXzZ7++LY59+/b27E8nDEMaJSH5z6+uBwBAzWu3fVXAHgKCioAqdBWxI0CINahruqq022fEWZGUlHr5nCIBo3lyPh6HS0lA8S3C7xN+5Yh4zL5/fL6cz4NZClRX8wsEQTzkc1b1mbEc10BFUlfVY1sfu756/weTj68UQgQAAA==
```

