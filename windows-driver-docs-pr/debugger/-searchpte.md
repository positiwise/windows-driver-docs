---
title: searchpte (WinDbg)
description: The searchpte extension searches physical memory for the specified page frame number (PFN).
keywords: ["searchpte Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- searchpte
api_type:
- NA
---

# !searchpte


The **!searchpte** extension searches physical memory for the specified page frame number (PFN).

```dbgcmd
!searchpte PFN 
!searchpte -?
```

## <span id="Parameters"></span><span id="parameters"></span><span id="PARAMETERS"></span>Parameters


<span id="_______PFN______"></span><span id="_______pfn______"></span> *PFN*   
Specifies the PFN in hexadecimal format.

<span id="_______-_______"></span> **-?**   
Displays help for this extension in the Debugger Command window.

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

 

### <span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>Additional Information

For information about page tables and page directories, see *Microsoft Windows Internals*, by Mark Russinovich and David Solomon. 

## Remarks

To stop execution at any time, press CTRL+BREAK (in WinDbg) or CTRL+C (in KD).

 

 





