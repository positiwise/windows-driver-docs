---
title: cchelp (WinDbg)
description: The cchelp extension displays some brief Help text in the Debugger command window for some of the cache management extensions.
keywords: ["cache manager", "cchelp Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
ms.topic: reference
api_name:
- cchelp
api_type:
- NA
---

# !cchelp


The **!cchelp** extension displays some brief Help text in the Debugger command window for some of the cache management extensions.

```dbgsyntax
!cchelp
```

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

For information about cache management, see the Microsoft Windows SDK documentation and *Microsoft Windows Internals* by Mark Russinovich and David Solomon.

The **!cchelp** extension displays help for the [**!bcb**](-bcb.md), [**!defwrites**](-defwrites.md), [**!finddata**](-finddata.md), and [**!scm**](-scm.md) cache management extensions. Other cache management extensions include [**!openmaps**](-openmaps.md) and [**!pcm**](-pcm.md).

 

 





