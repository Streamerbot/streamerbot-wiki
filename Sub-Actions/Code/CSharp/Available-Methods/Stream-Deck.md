---
title: Stream Deck
description: C# Available Methods Reference
published: true
date: 2023-05-18T16:18:36.001Z
tags: 
editor: markdown
dateCreated: 2023-05-18T16:18:33.833Z
---

## Background
### Background Color
```csharp
void StreamDeckSetBackgroundColor(string buttonId, string color);
void StreamDeckSetBackgroundColor(string buttonId, string color, int state);
```

### Background Image Url
```csharp
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl, string color);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl, int state);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl, string color, int state);
```

### Background Image File Path
```csharp
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile, string color);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile, int state);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile, string color, int state);
```

## Title
```csharp
void StreamDeckSetTitle(string buttonId, string title);
void StreamDeckSetTitle(string buttonId, string title, int state);
```

## State
```csharp
void StreamDeckSetState(string buttonId, int state);
void StreamDeckToggleState(string buttonId);
```

## Value
```csharp
void StreamDeckSetValue(string buttonId, string value);
```

## Alert
```csharp
void StreamDeckShowAlert(string buttonId);
```

## Ok
```csharp
void StreamDeckShowOk(string buttonId);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}