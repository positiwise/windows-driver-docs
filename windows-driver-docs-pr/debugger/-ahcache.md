---
title: ahcache (WinDbg)
description: The ahcache extension displays the application compatibility cache.
keywords: ["ahcache Windows Debugging"]
ms.date: 09/17/2018
topic_type:
- apiref
ms.topic: reference
api_name:
- ahcache
api_type:
- NA
---

# !ahcache


The **!ahcache** extension displays the application compatibility cache.

```dbgcmd
!ahcache [Flags] 
```

## <span id="ddk__ahcache_dbg"></span><span id="DDK__AHCACHE_DBG"></span>Parameters


<span id="_______Flags______"></span><span id="_______flags______"></span><span id="_______FLAGS______"></span> *Flags*   
Specifies the information to include in the display. This can be any combination of the following bits (the default is zero):

<span id="Bit_0__0x1_"></span><span id="bit_0__0x1_"></span><span id="BIT_0__0X1_"></span>Bit 0 (0x1)  
Displays the RTL\_GENERIC\_TABLE list instead of the LRU list.

<span id="Bit_4__0x10_"></span><span id="bit_4__0x10_"></span><span id="BIT_4__0X10_"></span>Bit 4 (0x10)  
Verbose display: includes all entry details, not just the names.

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

 

 

 





