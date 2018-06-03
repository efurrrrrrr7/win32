---
Description: This section describes the enumerations and structures that are supported by the Energy Measurement Interface (EMI).
ms.assetid: B644E470-5744-4051-868D-F33EA821BA12
title: EMI Enumerations and Structures
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# EMI Enumerations and Structures

This section describes the enumerations and structures that are supported by the Energy Measurement Interface (EMI).

## In this section



| Topic                                                             | Description                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EMI\_MEASUREMENT\_DATA**](/windows/desktop/api/emi/ns-emi-emi_measurement_data)<br/> | The [**EMI\_MEASUREMENT\_DATA**](/windows/desktop/api/emi/ns-emi-emi_measurement_data) structure provides data about the current energy measurement and the time at which the measurement was taken.<br/>                                                                                         |
| [**EMI\_MEASUREMENT\_UNIT**](/windows/desktop/api/emi/ne-emi-emi_measurement_unit)<br/> | The [**EMI\_MEASUREMENT\_UNIT**](/windows/desktop/api/emi/ne-emi-emi_measurement_unit) enumeration represents the available units of energy measurements that can be retrieved from a device by using [**IOCTL\_EMI\_GET\_MEASUREMENT**](/windows/desktop/api/emi/ni-emi-ioctl_emi_get_measurement). <br/>                    |
| [**EMI\_METADATA**](/windows/desktop/api/emi/ns-emi-emi_metadata)<br/>                  | The [**EMI\_METADATA**](/windows/desktop/api/emi/ns-emi-emi_metadata) structure provides metadata about a device that supports the Energy Metering Interface (EMI) interface, such as the hardware model and hardware revision.<br/>                                                              |
| [**EMI\_METADATA\_SIZE**](/windows/desktop/api/emi/ns-emi-emi_metadata_size)<br/>       | The [**EMI\_METADATA\_SIZE**](/windows/desktop/api/emi/ns-emi-emi_metadata_size) structure specifies the size of the Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an [**IOCTL\_EMI\_GET\_METADATA**](/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata) request.<br/> |
| [**EMI\_VERSION**](/windows/desktop/api/emi/ns-emi-emi_version)<br/>                    | The [**EMI\_VERSION**](/windows/desktop/api/emi/ns-emi-emi_version) structure describes the version of the Energy Metering Interface (EMI) that is supported by a device.<br/>                                                                                                                    |



 

> [!Note]  
> The EMI enumerations and structures are supported in Windows 10 and later versions of the Windows operating systems.

 

## Related topics

<dl> <dt>

[Energy Metering Interface](energy-metering-interface.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bpowermeter\powermeter%5D:%20EMI%20Enumerations%20and%20Structures%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/en-us/default.aspx. "Send comments about this topic to Microsoft")




