---
title: DriverEntry of IDE Controller Minidriver function
description: DriverEntry initializes the minidriver.
keywords: ["DriverEntry function Storage Devices"]
topic_type:
- apiref
ms.topic: reference
api_name:
- DriverEntry
api_location:
- NtosKrnl.exe
api_type:
- DllExport
ms.date: 10/17/2018
---

# DriverEntry of IDE Controller Minidriver function


**DriverEntry** initializes the minidriver.

## Syntax

```ManagedCPlusPlus
NTSTATUS DriverEntry(
  _In_ PDRIVER_OBJECT  DriverObject,
  _In_ PUNICODE_STRING RegistryPath
);
```

## Parameters

*DriverObject* \[in\]  
Contains a pointer to the IDE controller minidriver's driver object.

*RegistryPath* \[in\]  
Specifies a string indicating the registry path to the driver's configuration information in the registry.

## Return value

**DriverEntry** returns STATUS\_SUCCESS if successful; otherwise it returns the error code received from the [**PciIdeXInitialize**](/previous-versions/windows/hardware/drivers/ff563788(v=vs.85)) library routine.

## Remarks

Each controller minidriver must have a routine named **DriverEntry** in order to load.

An IDE controller minidriver's **DriverEntry** routine must call the [**PciIdeXInitialize**](/previous-versions/windows/hardware/drivers/ff563788(v=vs.85)) library routine. **PciIdeXInitialize** initializes the controller minidriver's dispatch tables, allocates an extension for the *DriverObject*, and stores various values in the driver object's extension. Values that must be stored in the driver object's extension include the size of the driver extension and a pointer to a controller minidriver [**HwIdeXGetControllerProperties**](/previous-versions/windows/hardware/drivers/ff557254(v=vs.85)) routine that retrieves information about the IDE controller.

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Target platform</p></td>
<td align="left">Desktop</td>
</tr>
<tr class="even">
<td align="left"><p>Header</p></td>
<td align="left">Ide.h (include Ide.h)</td>
</tr>
<tr class="odd">
<td align="left"><p>Library</p></td>
<td align="left">NtosKrnl.lib</td>
</tr>
<tr class="even">
<td align="left"><p>DLL</p></td>
<td align="left">NtosKrnl.exe</td>
</tr>
</tbody>
</table>

## <span id="see_also"></span>See also


[**HwIdeXGetControllerProperties**](/previous-versions/windows/hardware/drivers/ff557254(v=vs.85))

[**IDE\_CONTROLLER\_PROPERTIES**](/previous-versions/windows/hardware/drivers/ff559076(v=vs.85))

[**PciIdeXInitialize**](/previous-versions/windows/hardware/drivers/ff563788(v=vs.85))

 

