---
title: Test
description: Official Documentation for Streamer.bot
published: false
date: 2022-09-09T14:00:55.899Z
tags: 
editor: markdown
dateCreated: 2022-09-08T09:52:37.686Z
---

# Application
## General
```csharp
int Between(int min, int max);
double NextDouble(); // get a random value between 0f and 1f
```

```csharp
void Wait(int milliseconds);
```

```csharp
string UrlEncode(string text);
string EscapeString(string text);
```

<pre class="prismjs line-numbers language-csharp"><code class="language-csharp"><span class="token return-type class-name">EventSource</span> <span class="token function">GetSource</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token return-type class-name">EventType</span> <span class="token function">GetEventType</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span aria-hidden="true" class="line-numbers-rows"><span></span><span></span></span></code></pre>