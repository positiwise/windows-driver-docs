---
title: wdfkd.wdfumfile
description: The wdfkd.wdfumfile extension displays information about a UMDF intra-stack file.
keywords: ["wdfkd.wdfumfile Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- wdfkd.wdfumfile
api_type:
- NA
---

# !wdfkd.wdfumfile


The **!wdfkd.wdfumfile** extension displays information about a UMDF intra-stack file.

```dbgcmd
!wdfkd.wdfumfile Address 
```

## <span id="Parameters"></span><span id="parameters"></span><span id="PARAMETERS"></span>Parameters


<span id="_______Address______"></span><span id="_______address______"></span><span id="_______ADDRESS______"></span> *Address*   
Specifies the address of the UMDF intra-stack file to display information about.

## <span id="DLL"></span><span id="dll"></span>DLL


Wdfkd.dll

## <span id="Frameworks"></span><span id="frameworks"></span><span id="FRAMEWORKS"></span>Frameworks


UMDF 2

## <span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>Additional Information


For more information, see [Kernel-Mode Driver Framework Debugging](kernel-mode-driver-framework-debugging.md).

## Remarks

You can use this command in a kernel-mode debugging session or in a user-mode debugging session that is attached to the UMDF host process (wudfhost.exe).

This command displays the same information as the user-mode command [**!wudfext.umfile**](-wudfext-umfile.md).

 

 





