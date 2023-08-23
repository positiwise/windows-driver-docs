---
title: gpiokd.pinisrvec
description: The gpiokd.pinisrvec command displays Interrupt Service Routine (ISR) vector information for a specified pin.
keywords: ["gpiokd.pinisrvec Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- gpiokd.pinisrvec
api_type:
- NA
---

# !gpiokd.pinisrvec


The **!gpiokd.pinisrvec** command displays Interrupt Service Routine (ISR) vector information for a specified pin.

```dbgcmd
!gpiokd.bankinfo PinAddress
```

## <span id="ddk__devobj_dbg"></span><span id="DDK__DEVOBJ_DBG"></span>Parameters


<span id="_______PinAddress______"></span><span id="_______pinaddress______"></span><span id="_______PINADDRESS______"></span> *PinAddress*   
Address of the [\_GPIO\_PIN\_INFORMATION\_ENTRY](gpio-extensions.md#data-structures-used-by-the-gpio-commands) data structure that represents the pin.

## <span id="DLL"></span><span id="dll"></span>DLL


Gpiokd.dll

## <span id="see_also"></span>See also


[GPIO Extensions](gpio-extensions.md)

 

 






