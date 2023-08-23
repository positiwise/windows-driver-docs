---
title: srb (WinDbg)
description: The srb extension displays information about a SCSI Request Block (SRB).
keywords: ["srb Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- srb
api_type:
- NA
---

# !srb


The **!srb** extension displays information about a SCSI Request Block (SRB).

```dbgcmd
!srb Address 
```

## <span id="ddk__srb_dbg"></span><span id="DDK__SRB_DBG"></span>Parameters


<span id="_______Address______"></span><span id="_______address______"></span><span id="_______ADDRESS______"></span> *Address*   
Specifies the hexadecimal address of the SRB on the target computer.

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

 

### <span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>Additional Information

For information about SRBs, see the Windows Driver Kit (WDK) documentation.

## Remarks

An SRB is a system-defined structure used to communicate I/O requests from a SCSI class driver to a SCSI port driver.

 

 





