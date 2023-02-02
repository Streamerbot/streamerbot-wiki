---
title: Discord
description: C# Available Methods Reference
published: true
date: 2023-02-02T01:22:48.299Z
tags: 
editor: markdown
dateCreated: 2022-10-29T21:03:50.261Z
---

## Post Text To Webhook
### Tabset {.tabset}
#### Code
```csharp
bool DiscordPostTextToWebhook(string webhookUrl, string content, string username = null, bool textToSpeech = false);
```

#### Example
```csharp
let result = CPH.DiscordPostTextToWebhook("webhookUrl", "content", "username" / null, true/false);
```

### End Tabset {.tabset}

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}