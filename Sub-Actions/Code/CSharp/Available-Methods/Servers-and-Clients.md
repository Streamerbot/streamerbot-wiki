---
title: Servers and Clients
description: C# Available Methods Reference
published: true
date: 2022-10-29T20:46:01.700Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:46:01.700Z
---

## Websocket Server
```csharp
void WebsocketBroadcastString(string data); // send a custom event over the websocket server
void WebsocketBroadcastJson(string data); // send a custom event over the websocket server
```

## Websocket Clients
```csharp
void WebsocketConnect(int connection = 0);
void WebsocketDisconnect(int connection = 0);
bool WebsocketIsConnected(int connection = 0);
void WebsocketSend(string data, int connection = 0);
void WebsocketSend(byte[] data, int connection = 0);
```

## Custom Websocket Servers
```csharp
void WebsocketCustomServerStart(int connection = 0);
void WebsocketCustomServerStop(int connection = 0);
bool WebsocketCustomServerIsListening(int connection = 0);
void WebsocketCustomServerCloseAllSessions(int connection = 0);
void WebsocketCustomServerCloseSession(string sessionId, int connection = 0);
void WebsocketCustomServerBroadcast(string data, string sessionId, int connection = 0);
```

```csharp
int WebsocketCustomServerGetConnectionByName(string name);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}