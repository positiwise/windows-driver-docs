---
title: rcdrkd.rcdrsearchpath
description: The rcdrkd.rcdrsearchpath extension sets the search path for trace message format (TMF) and trace message control (TMC) files.
keywords: ["rcdrkd.rcdrsearchpath Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- rcdrkd.rcdrsearchpath
api_type:
- NA
---

# !rcdrkd.rcdrsearchpath


The **!rcdrkd.rcdrsearchpath** extension sets the search path for trace message format (TMF) and trace message control (TMC) files.

```dbgcmd
!rcdrkd.rcdrsearchpath FilePath
```

## <span id="ddk__devobj_dbg"></span><span id="DDK__DEVOBJ_DBG"></span>Parameters


<span id="_______FilePath______"></span><span id="_______filepath______"></span><span id="_______FILEPATH______"></span> *FilePath*   
Path to the format files.

## <span id="DLL"></span><span id="dll"></span>DLL


Rcdrkd.dll

## Remarks

The search path set by this command takes precedence over the search path specified in the TRACE\_FORMAT\_SEARCH\_PATH environment variable.

## <span id="see_also"></span>See also


[RCDRKD Extensions](rcdrkd-extensions.md)

 

 






