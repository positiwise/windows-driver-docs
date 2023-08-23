---
title: .secure (Activate Secure Mode)
description: The .secure command activates or displays the status of Secure Mode.
keywords: [".secure (Activate Secure Mode) Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- .secure (Activate Secure Mode)
api_type:
- NA
---

# .secure (Activate Secure Mode)


The **.secure** command activates or displays the status of Secure Mode.

```dbgcmd
.secure 1 
.secure 
```

## <span id="ddk_meta_activate_secure_mode_dbg"></span><span id="DDK_META_ACTIVATE_SECURE_MODE_DBG"></span>


### <span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Environment

Secure Mode can only be enabled while the debugger is dormant. Secure Mode applies only to kernel-mode sessions because, by definition, Secure Mode prevents user-mode debugging operations.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Modes</strong></p></td>
<td align="left"><p>kernel mode only</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Targets</strong></p></td>
<td align="left"><p>live, crash dump</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Platforms</strong></p></td>
<td align="left"><p>all</p></td>
</tr>
</tbody>
</table>

 

### <span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>Additional Information

For details, see [Secure Mode](secure-mode.md).

## Remarks

To activate Secure Mode, use the command **.secure 1** (or **.secure** followed by any nonzero value).

The command **.secure** will show whether Secure Mode is currently active.

 

 





