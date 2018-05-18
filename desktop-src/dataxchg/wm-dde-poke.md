---
title: WM\_DDE\_POKE message
description: A Dynamic Data Exchange (DDE) client application posts a WM\_DDE\_POKE message to a DDE server application.
ms.assetid: '848142b7-a7ef-4206-9bb3-b511388cfaaa'
keywords: ["WM_DDE_POKE message Data Exchange"]
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
---

# WM\_DDE\_POKE message

A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application. A client uses this message to request the server to accept an unsolicited data item. The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.

To post this message, call the [**PostMessage**](https://msdn.microsoft.com/library/windows/desktop/ms644944) function with the following parameters.


```C++
#define WM_DDE_POKE        0x03E7
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

A handle to the client window posting the message.

</dd> <dt>

*lParam* 
</dt> <dd>

The low-order word is a handle to a global memory object containing a [**DDEPOKE**](ddepoke.md) structure with the data and additional information.

The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.

</dd> </dl>

## Remarks

### Posting

The client application must allocate memory for the global memory object using the [**GlobalAlloc**](https://msdn.microsoft.com/library/windows/desktop/aa366574) function. The client application must delete the object if either of the following conditions is true:

-   The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.
-   The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).

The client application must create the atom using the [**GlobalAddAtom**](globaladdatom.md) function.

The client application must create or reuse the **WM\_DDE\_POKE**�*lParam* parameter by calling the [**PackDDElParam**](packddelparam.md) function or the [**ReuseDDElParam**](reuseddelparam.md) function.

### Receiving

The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively. When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.

The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md)�*lParam* parameter by calling the [**PackDDElParam**](packddelparam.md) function or the [**ReuseDDElParam**](reuseddelparam.md) function.

To free the global memory object, the server should call the [**GlobalFree**](https://msdn.microsoft.com/library/windows/desktop/aa366579) function. Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md#standard-clipboard-formats) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](https://msdn.microsoft.com/library/windows/desktop/dd183537) with the embedded metafile handle. These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](metafilepict.md) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.

To free the object, the server should call the [**FreeDDElParam**](freeddelparam.md) function.

## Requirements



|                                     |                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�2000 Professional \[desktop apps only\]<br/>                                           |
| Minimum supported server<br/> | Windows�2000 Server \[desktop apps only\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Dde.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

**Reference**
</dt> <dt>

[**DDEPOKE**](ddepoke.md)
</dt> <dt>

[**FreeDDElParam**](freeddelparam.md)
</dt> <dt>

[**GlobalAddAtom**](globaladdatom.md)
</dt> <dt>

[**METAFILEPICT**](metafilepict.md)
</dt> <dt>

[**PackDDElParam**](packddelparam.md)
</dt> <dt>

[**PostMessage**](https://msdn.microsoft.com/library/windows/desktop/ms644944)
</dt> <dt>

[**ReuseDDElParam**](reuseddelparam.md)
</dt> <dt>

[**SendMessage**](https://msdn.microsoft.com/library/windows/desktop/ms644950)
</dt> <dt>

[**UnpackDDElParam**](unpackddelparam.md)
</dt> <dt>

[**WM\_DDE\_ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[About Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

�

�




