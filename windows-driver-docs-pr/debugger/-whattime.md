---
title: whattime (WinDbg)
description: The whattime extension converts a tick count into a standard time value.
keywords: ["tick count", "whattime Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- whattime
api_type:
- NA
---

# !whattime


The **!whattime** extension converts a tick count into a standard time value.

```dbgcmd
!whattime Ticks
```

## <span id="Parameters"></span><span id="parameters"></span><span id="PARAMETERS"></span>Parameters


<span id="_______Ticks______"></span><span id="_______ticks______"></span><span id="_______TICKS______"></span> *Ticks*   
The number of ticks.

### <span id="DLL"></span><span id="dll"></span>DLL

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows 2000</strong></p></td>
<td align="left"><p>Unavailable</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows XP and later</strong></p></td>
<td align="left"><p>Kdexts.dll</p></td>
</tr>
</tbody>
</table>

 

## Remarks

The output is displayed as *HH:MM:SS.mmm*. Here is an example:

```dbgcmd
kd> !whattime 29857ae4
696613604 Ticks in Standard Time:  15:02:16.040s
```

 

 





