---
title: bthkd.sdpnode
description: The bthkd.sdpnode command displays information about a node in an sdp tree.
keywords: ["bthkd.sdpnode Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- bthkd.sdpnode
api_type:
- NA
---

# !bthkd.sdpnode


The **!bthkd.sdpnode** command displays information about a node in an sdp tree.

```dbgsyntax
!bthkd.sdpnode addr [flags]
```

## <span id="ddk__devobj_dbg"></span><span id="DDK__DEVOBJ_DBG"></span>Parameters


<span id="_______addr______"></span><span id="_______ADDR______"></span> *addr*   
Address of the sdp tree node to display.

<span id="_______flags______"></span><span id="_______FLAGS______"></span> *flags*   
0x1 - Recurse node

0x2 - Verbose

default is 0x0

## <span id="DLL"></span><span id="dll"></span>DLL


Bthkd.dll

## <span id="see_also"></span>See also


[Bluetooth Extensions (Bthkd.dll)](bluetooh-extensions--bthkd-dll-.md)

 

 






