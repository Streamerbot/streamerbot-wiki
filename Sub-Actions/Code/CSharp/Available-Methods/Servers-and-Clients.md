---
title: Servers and Clients
description: C# Available Methods Reference
published: true
date: 2022-12-14T16:55:41.478Z
tags: 
editor: markdown
dateCreated: 2022-10-29T20:46:01.700Z
---

## Websocket Server
```csharp
void WebsocketBroadcastString(string data); // send a custom event over the websocket server
void WebsocketBroadcastJson(string data); // send a custom event over the websocket server, used for browser widgets
```

## Websocket Clients
```csharp
void WebsocketConnect(int connection = 0);
void WebsocketDisconnect(int connection = 0);
```

```csharp
bool WebsocketIsConnected(int connection = 0);
```

```csharp
void WebsocketSend(string data, int connection = 0);
void WebsocketSend(byte[] data, int connection = 0);
```

## Custom Websocket Servers
```csharp
void WebsocketCustomServerStart(int connection = 0);
void WebsocketCustomServerStop(int connection = 0);
```

```csharp
bool WebsocketCustomServerIsListening(int connection = 0);
```

```csharp
void WebsocketCustomServerCloseAllSessions(int connection = 0);
void WebsocketCustomServerCloseSession(string sessionId, int connection = 0);
void WebsocketCustomServerBroadcast(string data, string sessionId, int connection = 0);
```

```csharp
int WebsocketCustomServerGetConnectionByName(string name);
```

## UDP Broadcast
```csharp
int BroadcastUdp(int port, object data);
```

---

- [<i class="mdi mdi-chevron-left"></i> **C# Available Methods *Go Back***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}