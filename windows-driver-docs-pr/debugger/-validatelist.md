---
title: validatelist
description: The validatelist extension verifies that the backward and forward links in a doubly-linked list are valid.
keywords: ["doubly-linked list", "validatelist Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- validatelist
api_type:
- NA
---

# !validatelist


The **!validatelist** extension verifies that the backward and forward links in a doubly-linked list are valid.

```dbgcmd
!validatelist Address
```

## <span id="Parameters"></span><span id="parameters"></span><span id="PARAMETERS"></span>Parameters


<span id="_______Address______"></span><span id="_______address______"></span><span id="_______ADDRESS______"></span> *Address*   
The address of the doubly-linked list.

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

To stop execution, press Ctrl+Break (in WinDbg) or Ctrl+C (in KD).

 

 





