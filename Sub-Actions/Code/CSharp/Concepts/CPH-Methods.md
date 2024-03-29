---
title: CPH Methods
description: Streamer.bot C# Concepts Reference
published: true
date: 2023-03-27T14:07:57.967Z
tags: 
editor: markdown
dateCreated: 2023-03-27T00:11:32.868Z
---

## Quick Links
- [<i class="mdi mdi-language-csharp primary--text"></i> **C# Available Methods *A list of all available C# methods***](/Sub-Actions/Code/CSharp/Available-Methods)
{.btn-grid .my-5}

## Overview
CPH Methods are used for communication between Streamer.bot and your C# code. These methods can be used for a lot of things that can be done with Sub-Actions or for even a couple things that don't have Sub-Actions. E.g. you can run actions, send messages to Twitch/YouTube and even do OBS raw.

## Structure
```diagram
PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHdpZHRoPSI0NjFweCIgaGVpZ2h0PSIyMTBweCIgdmlld0JveD0iLTAuNSAtMC41IDQ2MSAyMTAiIGNvbnRlbnQ9IiZsdDtteGZpbGUgaG9zdD0mcXVvdDtlbWJlZC5kaWFncmFtcy5uZXQmcXVvdDsgbW9kaWZpZWQ9JnF1b3Q7MjAyMy0wMy0yN1QwMDoxODowNi4zMTBaJnF1b3Q7IGFnZW50PSZxdW90O01vemlsbGEvNS4wIChXaW5kb3dzIE5UIDEwLjA7IFdpbjY0OyB4NjQpIEFwcGxlV2ViS2l0LzUzNy4zNiAoS0hUTUwsIGxpa2UgR2Vja28pIENocm9tZS8xMTEuMC4wLjAgU2FmYXJpLzUzNy4zNiZxdW90OyBldGFnPSZxdW90O2tXMVRBUm9WeXFCVEN3bkx2ZUhXJnF1b3Q7IHZlcnNpb249JnF1b3Q7MjEuMS4xJnF1b3Q7IHR5cGU9JnF1b3Q7ZW1iZWQmcXVvdDsmZ3Q7Jmx0O2RpYWdyYW0gaWQ9JnF1b3Q7NG1KRUpMWTJoUERYNHhIUEMxd3MmcXVvdDsgbmFtZT0mcXVvdDtQYWdlLTEmcXVvdDsmZ3Q7N1ZsTmM2czJGUDAxekxTYk4zd0ViQzlqTzBrWFNkdHBPbTNmVW9ZTHFKRVJGU0syOCtzcklXRkE0R2ZHaitRdFludGhPSktPeEwzM0hNbTI1YTIyK3dlRzh2U0pSa0FzMTQ3MmxyZTJYTmV4ZlZ0OFNPU2drTUFMRkpBd0hPbE9EZkNNMzZBZXFkRVNSMUIwT25KS0NjZDVGd3hwbGtISU94aGlqTzY2M1dKS3VyUG1LSUVlOEJ3aTBrZi94aEZQRlRxdkgwdml2d0JPMG5wbXg5WXRXMVIzMWtDUm9vanVXcEIzWjNrclJpbFhWOXY5Q29nTVhoMFhOZTcrUk90eFlRd3lQbWFBcXdhOElsTHFaN1BjZ0lpaHk1Z0tCaGxDUWxuVkV2eFh5bFV0TGRlYmIyQVJSMjBvU09SbndSbk9Fa3ZPcVVqRXhJcEh0WS9oanAwWXpjTSs5eFB3bEVhL29pMmNJUC9wUjY4Y29YQU9OMzN1S3JpL1phZldiYm1yMXJ5WExINGphdjhrK1NqbWJ5Nzl6eDM5enBSV3J6Njc2amQxdU1VbjJ1YmlJdHNVZVl2cmdpazIwY0tMRi8wcE9DdFBaZlBuQ3Fxa3pRKzFYekJhWmhGSXlUbHlSa3pJNmppZFo5L0t0OEFSd1VrbXNGQm9GMFRqTXFVTXZ3bHVSUFJJZ2paQWxpaDhTU3JHbWlTam9yanFWc29pWUViTExzVWNubk1VeXZYc2hDZExjcjZ0YWVYNld3dTZuOG0zRklVWUlWVHhDTEgwRXZ2NFpHMTcwWTd6Q296RHZnVnB1M2tBdWdYT0RxS0xicTJkNzlDMTlGM2pvemVCeHRLV2g5WVkwdGFkSElrYmR4TVgydUNHemM0Yk1Ec2pVNUJGdDNLRGtHa2dxQ2h3MkExVmswbDdJSEMyZkNzM29TL1Ficm0zeGV0YkFZU29zK1gwdzljS2tEOFFueHBqUUJESHI5Mk5haWhvZW9iZkthN3EvN2czZTBaNlpsMktncFlzQkQycXZiR2NJZklOSG81WUFyekhVNlh3K05TanNucHowUloyeXBQK0FGNnlyR2JZc0JyL3E2SS9aU1ZHRlFrcDhHN2Q5TFF0QllQRmllSldOMnh4Rk1uaFN3WUZma09iaWtwV1RDNURWQVhOWDFyK1duS1ZuQmJxVE9UMGlrMHJ2dTB4R3BwQXV6T2pPQWJFTzZUZG13bTA2MSsxZTFhN3ZtdG9kMzZoZGcwaTMrQ1pUcnZCcE5wdEh3NGI1ZEpZZmoxSVFSNi9xelBrNVNvZUs3WHhhaC9hbWJ0MU9vRnNIZGNvRENjWXBWdHZBdDNPcnJvOXAxdWh0MjU2WmtiY3grcldKSG8vM2M2dldUMmJWWDloWk5XNU1Lc0dVWDA3ZlZZWGs3cnhHbkYweUU4Yk1pNEdtbktPYWZiNURIcG1PTURjNlJuMHpIMGZnNjdQY0IreEIxOVQzcWphczgrbS9MMzJaTWZwdTdVd3pXZDlTNWs0SlNVMFErU3VRWTBJTkgwZUtjMTFLdjRGemcvNjExcjVKYVdiS05oai9vOGMvc1hYZDE5YkxldTlacTV1RHVjQ3JjeXpXOEhLQ0x2WTJjMWd0TXVQRHU3MVY0YXplNk8zTUlyLzBoT1BTZlIrSng1bjJwOFoxaENqa3ZDK0hTcCsxNWFPYWJZcEE3VS9xV042d1ljNXByaHQvb0pSeGRMOGtlWGQvUTg9Jmx0Oy9kaWFncmFtJmd0OyZsdDsvbXhmaWxlJmd0OyI+PGRlZnMvPjxnPjxyZWN0IHg9IjAiIHk9IjAiIHdpZHRoPSI0NjAiIGhlaWdodD0iNjAiIHJ4PSI5IiByeT0iOSIgZmlsbD0iIzBhMGEwYSIgc3Ryb2tlPSJyZ2IoMCwgMCwgMCkiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiIHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogNDU4cHg7IGhlaWdodDogMXB4OyBwYWRkaW5nLXRvcDogMzBweDsgbWFyZ2luLWxlZnQ6IDFweDsiPjxkaXYgZGF0YS1kcmF3aW8tY29sb3JzPSJjb2xvcjogI0Y3RjdGNzsgIiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwcHg7IHRleHQtYWxpZ246IGNlbnRlcjsiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogcmdiKDI0NywgMjQ3LCAyNDcpOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyBvdmVyZmxvdy13cmFwOiBub3JtYWw7Ij48Zm9udCBjb2xvcj0iIzhiZTlmZCI+c3RyaW5nIDwvZm9udD48Zm9udCBjb2xvcj0iI2YxZmE4YyI+TWV0aG9kTmFtZTwvZm9udD4oPGZvbnQgY29sb3I9IiM4YmU5ZmQiPnN0cmluZyA8L2ZvbnQ+PGZvbnQgY29sb3I9IiNhYWM4ZTQiPnZhbHVlT25lPC9mb250PiwgPGZvbnQgY29sb3I9IiM4YmU5ZmQiPmJvb2w8L2ZvbnQ+IDxmb250IGNvbG9yPSIjYWFjOGU0Ij52YWx1ZVR3byA8L2ZvbnQ+PGZvbnQgY29sb3I9IiNmZmZmZmYiPj08L2ZvbnQ+PGZvbnQgY29sb3I9IiNhYWM4ZTQiPsKgPC9mb250Pjxmb250IGNvbG9yPSIjYmQ5M2Y5Ij50cnVlPC9mb250Pik7PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjIzMCIgeT0iMzQiIGZpbGw9IiNGN0Y3RjciIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTJweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+c3RyaW5nIE1ldGhvZE5hbWUoc3RyaW5nIHZhbHVlT25lLCBib29sIHZhbHVlVHdvID3CoHRydWUpOzwvdGV4dD48L3N3aXRjaD48L2c+PHBhdGggZD0iTSA4MyA5NyBMIDgzIDUzLjM3IiBmaWxsPSJub25lIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gODMgNDguMTIgTCA4Ni41IDU1LjEyIEwgODMgNTMuMzcgTCA3OS41IDU1LjEyIFoiIGZpbGw9IiNmZjAwMDAiIHN0cm9rZT0iI2ZmMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PHJlY3QgeD0iNTMiIHk9IjEwMCIgd2lkdGg9IjYwIiBoZWlnaHQ9IjQwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiIHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogMXB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDEyMHB4OyBtYXJnaW4tbGVmdDogODNweDsiPjxkaXYgZGF0YS1kcmF3aW8tY29sb3JzPSJjb2xvcjogcmdiKDAsIDAsIDApOyAiIHN0eWxlPSJib3gtc2l6aW5nOiBib3JkZXItYm94OyBmb250LXNpemU6IDBweDsgdGV4dC1hbGlnbjogY2VudGVyOyI+PGRpdiBzdHlsZT0iZGlzcGxheTogaW5saW5lLWJsb2NrOyBmb250LXNpemU6IDEycHg7IGZvbnQtZmFtaWx5OiBIZWx2ZXRpY2E7IGNvbG9yOiByZ2IoMCwgMCwgMCk7IGxpbmUtaGVpZ2h0OiAxLjI7IHBvaW50ZXItZXZlbnRzOiBhbGw7IHdoaXRlLXNwYWNlOiBub3dyYXA7Ij48Zm9udCBjb2xvcj0iI2ZmZmZmZiI+UmV0dXJuPGJyIC8+VmFsdWU8L2ZvbnQ+PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjgzIiB5PSIxMjQiIGZpbGw9InJnYigwLCAwLCAwKSIgZm9udC1mYW1pbHk9IkhlbHZldGljYSIgZm9udC1zaXplPSIxMnB4IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5SZXR1cm4uLi48L3RleHQ+PC9zd2l0Y2g+PC9nPjxwYXRoIGQ9Ik0gMTMyIDk4IEwgMTMyIDU0LjM3IiBmaWxsPSJub25lIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gMTMyIDQ5LjEyIEwgMTM1LjUgNTYuMTIgTCAxMzIgNTQuMzcgTCAxMjguNSA1Ni4xMiBaIiBmaWxsPSIjZmYwMDAwIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxyZWN0IHg9IjEwMiIgeT0iMTA2IiB3aWR0aD0iNjAiIGhlaWdodD0iMzAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0wLjUgLTAuNSkiPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3QgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSIgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiA1OHB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDEyMXB4OyBtYXJnaW4tbGVmdDogMTAzcHg7Ij48ZGl2IGRhdGEtZHJhd2lvLWNvbG9ycz0iY29sb3I6IHJnYigwLCAwLCAwKTsgIiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwcHg7IHRleHQtYWxpZ246IGNlbnRlcjsiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogcmdiKDAsIDAsIDApOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyBvdmVyZmxvdy13cmFwOiBub3JtYWw7Ij48Zm9udCBjb2xvcj0iI2ZmZmZmZiI+TmFtZTxiciAvPm9mIHRoZSBtZXRob2Q8L2ZvbnQ+PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjEzMiIgeT0iMTI1IiBmaWxsPSJyZ2IoMCwgMCwgMCkiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTJweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+TmFtZS4uLjwvdGV4dD48L3N3aXRjaD48L2c+PHBhdGggZD0iTSAxOTUgMTYwIEwgMTk1IDU0LjM3IiBmaWxsPSJub25lIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gMTk1IDQ5LjEyIEwgMTk4LjUgNTYuMTIgTCAxOTUgNTQuMzcgTCAxOTEuNSA1Ni4xMiBaIiBmaWxsPSIjZmYwMDAwIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxwYXRoIGQ9Ik0gMjM5IDE2MSBMIDIzOSA1NS4zNyIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjZmYwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJzdHJva2UiLz48cGF0aCBkPSJNIDIzOSA1MC4xMiBMIDI0Mi41IDU3LjEyIEwgMjM5IDU1LjM3IEwgMjM1LjUgNTcuMTIgWiIgZmlsbD0iI2ZmMDAwMCIgc3Ryb2tlPSIjZmYwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48cmVjdCB4PSIxNTUiIHk9IjE3MSIgd2lkdGg9IjcyIiBoZWlnaHQ9IjMwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMC41IC0wLjUpIj48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiIHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogNzBweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiAxODZweDsgbWFyZ2luLWxlZnQ6IDE1NnB4OyI+PGRpdiBkYXRhLWRyYXdpby1jb2xvcnM9ImNvbG9yOiByZ2IoMCwgMCwgMCk7ICIgc3R5bGU9ImJveC1zaXppbmc6IGJvcmRlci1ib3g7IGZvbnQtc2l6ZTogMHB4OyB0ZXh0LWFsaWduOiBjZW50ZXI7Ij48ZGl2IHN0eWxlPSJkaXNwbGF5OiBpbmxpbmUtYmxvY2s7IGZvbnQtc2l6ZTogMTJweDsgZm9udC1mYW1pbHk6IEhlbHZldGljYTsgY29sb3I6IHJnYigwLCAwLCAwKTsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgb3ZlcmZsb3ctd3JhcDogbm9ybWFsOyI+PGZvbnQgY29sb3I9IiNmZmZmZmYiPkRhdGF5cGU8YnIgLz5vZiB0aGlzPGJyIC8+b3B0aW9uPC9mb250PjwvZGl2PjwvZGl2PjwvZGl2PjwvZm9yZWlnbk9iamVjdD48dGV4dCB4PSIxOTEiIHk9IjE5MCIgZmlsbD0icmdiKDAsIDAsIDApIiBmb250LWZhbWlseT0iSGVsdmV0aWNhIiBmb250LXNpemU9IjEycHgiIHRleHQtYW5jaG9yPSJtaWRkbGUiPkRhdGF5cGUuLi48L3RleHQ+PC9zd2l0Y2g+PC9nPjxyZWN0IHg9IjIxMCIgeT0iMTcxIiB3aWR0aD0iNjAiIGhlaWdodD0iMzAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0wLjUgLTAuNSkiPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3QgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSIgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiA1OHB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDE4NnB4OyBtYXJnaW4tbGVmdDogMjExcHg7Ij48ZGl2IGRhdGEtZHJhd2lvLWNvbG9ycz0iY29sb3I6IHJnYigwLCAwLCAwKTsgIiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwcHg7IHRleHQtYWxpZ246IGNlbnRlcjsiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogcmdiKDAsIDAsIDApOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyBvdmVyZmxvdy13cmFwOiBub3JtYWw7Ij48Zm9udCBjb2xvcj0iI2ZmZmZmZiI+TmFtZTxiciAvPm9mIHRoaXM8YnIgLz5vcHRpb248L2ZvbnQ+PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjI0MCIgeT0iMTkwIiBmaWxsPSJyZ2IoMCwgMCwgMCkiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTJweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+TmFtZS4uLjwvdGV4dD48L3N3aXRjaD48L2c+PHBhdGggZD0iTSAzNzAgMTYwIEwgMzcwIDU0LjM3IiBmaWxsPSJub25lIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9InN0cm9rZSIvPjxwYXRoIGQ9Ik0gMzcwIDQ5LjEyIEwgMzczLjUgNTYuMTIgTCAzNzAgNTQuMzcgTCAzNjYuNSA1Ni4xMiBaIiBmaWxsPSIjZmYwMDAwIiBzdHJva2U9IiNmZjAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxyZWN0IHg9IjM0MCIgeT0iMTcxIiB3aWR0aD0iNjAiIGhlaWdodD0iMzAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKC0wLjUgLTAuNSkiPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3QgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSIgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiA1OHB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDE4NnB4OyBtYXJnaW4tbGVmdDogMzQxcHg7Ij48ZGl2IGRhdGEtZHJhd2lvLWNvbG9ycz0iY29sb3I6IHJnYigwLCAwLCAwKTsgIiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwcHg7IHRleHQtYWxpZ246IGNlbnRlcjsiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxMnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogcmdiKDAsIDAsIDApOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyBvdmVyZmxvdy13cmFwOiBub3JtYWw7Ij48Zm9udCBjb2xvcj0iI2ZmZmZmZiI+RGVmYXVsdDxiciAvPnZhbHVlIG9mPGJyIC8+dGhpcyBvcHRpb248L2ZvbnQ+PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjM3MCIgeT0iMTkwIiBmaWxsPSJyZ2IoMCwgMCwgMCkiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTJweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+RGVmYXVsdC4uLjwvdGV4dD48L3N3aXRjaD48L2c+PC9nPjxzd2l0Y2g+PGcgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ii8+PGEgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMCwtNSkiIHhsaW5rOmhyZWY9Imh0dHBzOi8vd3d3LmRpYWdyYW1zLm5ldC9kb2MvZmFxL3N2Zy1leHBvcnQtdGV4dC1wcm9ibGVtcyIgdGFyZ2V0PSJfYmxhbmsiPjx0ZXh0IHRleHQtYW5jaG9yPSJtaWRkbGUiIGZvbnQtc2l6ZT0iMTBweCIgeD0iNTAlIiB5PSIxMDAlIj5UZXh0IGlzIG5vdCBTVkcgLSBjYW5ub3QgZGlzcGxheTwvdGV4dD48L2E+PC9zd2l0Y2g+PC9zdmc+
```


### Return Value
This is the return value of the method, this can be anything from void to string to a class or even an int. Most of the times you can ignore this but for some cases this can be useful

Docs 1:
```csharp
bool ActionExists(string actionName);
```

Example 1:
```csharp
bool actionExist = CPH.ActionExists("my action");

if (actionExist) {
  CPH.LogInfo("Action exists");
} else {
  CPH.LogInfo("Action doesn't exists");
}
```

Docs 2:
```csharp
void Wait(int milliseconds);
```

Example 2:
```csharp
// If the return value is `void` you can't put it in a C# variable
CPH.Wait(5000);
```

### Name of the Method
This is the name of the method

### Datatype of this option
This is the datatype that this option should be in this can be everything like a string, int, bool, etc.

### Name of this option
This is the name of the option, this isn't used in your code. This is just so you can see what should be in the place of the option

### Default value of this option
If the option is like this: `string option = "value"` so it ends with `= <value>` then you can remove the option if it's the same as the default value.

Docs 1:
```csharp
bool RunAction(string actionName, bool runImmediately = true);
```

Example 1:
```csharp
// As you see the `bool runImmediately = true` is removed here, because you may don't need to change the value of `runImmediately`
CPH.RunAction("my action");
```

Docs 2:
```csharp
void ObsSetScene(string sceneName, int connection = 0);
```

Example 2:
```csharp
// As you see the `int connection = 0` is removed here, because you might only have one connection so it doesn't matter
CPH.ObsSetScene("Camera Scene");
```

## Extra Examples
### Example 1
#### Docs
```csharp
bool TwitchAddVip(string userName);
```

#### Example
For full docs about the `args[]` below go to [this page](/Sub-Actions/Code/CSharp/Streamerbot-Variables)

```csharp
string user = args["userName"].ToString(); // This grabs the `userName` variable from the action, NOTE: if the variable doesn't exist the code will stop
bool vipSuccess = CPH.TwitchAddVip(user); // This adds the user as a vip and stores if it succeeds in `vipSuccess`

if (vipSuccess) { // Everything inside this if statement only runs if the user has successfully been added a vip
	CPH.SendMessage($"Added {user} as a vip");
}
```
