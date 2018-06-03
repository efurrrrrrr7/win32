---
Description: The Win32\_SystemSystemDriver association WMI class relates a computer system and a system driver running on that computer system.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Win32\_SystemSystemDriver class
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Win32\_SystemSystemDriver class

The **Win32\_SystemSystemDriver** association [WMI class](https://msdn.microsoft.com/windows/desktop/cfe4bcca-692e-45cd-a840-93ebfe4ae267) relates a computer system and a system driver running on that computer system.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties and methods are in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## Members

The **Win32\_SystemSystemDriver** class has these types of members:

-   [Properties](#properties)

### Properties

The **Win32\_SystemSystemDriver** class has these properties.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Data type: **Win32\_ComputerSystem**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/windows/desktop/838d295f-e812-4e46-99a4-d2714a0ae8dc), [**Override**](https://msdn.microsoft.com/windows/desktop/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("GroupComponent"), [**MappingStrings**](https://msdn.microsoft.com/windows/desktop/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("WMI\|Win32\_ComputerSystem")
</dt> </dl>

Reference to the instance representing the properties of the computer system upon which the driver is running.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Data type: **Win32\_SystemDriver**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/windows/desktop/838d295f-e812-4e46-99a4-d2714a0ae8dc), [**Override**](https://msdn.microsoft.com/windows/desktop/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("PartComponent"), [**MappingStrings**](https://msdn.microsoft.com/windows/desktop/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("WMI\|Win32\_SystemDriver")
</dt> </dl>

Reference to the instance representing the system driver running on the computer system.

</dd> </dl>

## Remarks

The **Win32\_SystemSystemDriver** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Operating System Classes](https://www.bing.com/search?q=Operating System Classes)
</dt> </dl>

 

 



