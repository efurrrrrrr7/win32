﻿---
Description: 'Provides access to the user property bag, if the property bag is present.'
ms.assetid: '6F181350-41A3-4592-BB72-1E3AD6FEC748'
title: 'IPrinterScriptContext::UserProperties property'
---

# IPrinterScriptContext::UserProperties property

Provides access to the user property bag, if the property bag is present.

This property is read-only.

## Syntax


```C++
HRESULT get_UserProperties(
  [out, retval]  IPrinterScriptablePropertyBag **ppPropertyBag
);
```



## Property value

The user property bag, if the property bag is present.

## Error codes

Returns an **HRESULT** value. If the property call was not successful, it returns the appropriate **HRESULT** error code.

## Remarks

The user property bag is not available in (constraint) JavaScript functions when the functions are called during de-spooling. Therefore JavaScript functions should be designed to handle the situation when there is a failure to retrieve the user property bag.

> [!Note]  
> Although the **UserProperties** property is read-only, the user property bag is a read/write property bag.

 

## Requirements



|                                     |                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8<br/>                                                                          |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                                |
| Header<br/>                   | <dl> <dt>Printerextension.h</dt> </dl> |



## See also

<dl> <dt>

[**IPrinterScriptablePropertyBag**](iprinterscriptablepropertybag.md)
</dt> <dt>

[**IPrinterScriptContext**](iprinterscriptcontext.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20IPrinterScriptContext::UserProperties%20property%20%20RELEASE:%20%285/12/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/en-us/default.aspx. "Send comments about this topic to Microsoft")




