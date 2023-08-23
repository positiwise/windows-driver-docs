---
title: amli ds (WinDbg)
description: The amli ds extension displays an AML stack.
keywords: ["amli ds Windows Debugging"]
ms.date: 09/17/2018
topic_type:
- apiref
ms.topic: reference
api_name:
- amli ds
api_type:
- NA
---

# !amli ds


The **!amli ds** extension displays an AML stack.

Syntax

```dbgcmd
    !amli ds [/v] [Address] 
```

## <span id="ddk__amli_ds_dbg"></span><span id="DDK__AMLI_DS_DBG"></span>Parameters


<span id="________v______"></span><span id="________V______"></span> **/v**   
Causes the display to be verbose. 

<span id="_______Address______"></span><span id="_______address______"></span><span id="_______ADDRESS______"></span> *Address*   
Specifies the address of the context block whose stack is desired. If *Address* is omitted, the current context is used.

### <span id="DLL"></span><span id="dll"></span>DLL

The !stacks extension displays information about the kernel stacks.

### <span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>Additional Information

For information about related commands and their uses, see [The AMLI Debugger](the-amli-debugger.md).

 

 





