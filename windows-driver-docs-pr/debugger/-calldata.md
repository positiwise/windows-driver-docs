---
title: calldata (WinDbg)
description: The calldata extension displays performance information in the form of procedure call statistics from the named table.
keywords: ["calldata Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- calldata
api_type:
- NA
---

# !calldata


The **!calldata** extension displays performance information in the form of procedure call statistics from the named table.

```dbgsyntax
    !calldata Table 
```

## <span id="ddk__calldata_dbg"></span><span id="DDK__CALLDATA_DBG"></span>Parameters


<span id="_______Table______"></span><span id="_______table______"></span><span id="_______TABLE______"></span> *Table*   
Name of the table that collects the call data.

### <span id="DLL"></span><span id="dll"></span>DLL

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows 2000</strong></p></td>
<td align="left"><p>Kdextx86.dll</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows XP and later</strong></p></td>
<td align="left"><p>Kdexts.dll</p></td>
</tr>
</tbody>
</table>

 

 

 





