---
Description: Determines whether the catalog is stopped.
ms.assetid: 2c113992-a49f-4370-a26c-c8ccd026e953
title: ICatAdm::IsCatalogStopped method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ICatAdm::IsCatalogStopped method

\[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/windows/desktop/6da601c6-3742-40ad-99f2-8817f7f642b3) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.\]

Determines whether the catalog is stopped.

## Syntax


```C++
HRESULT IsCatalogStopped(
  [out, retval] VARIANT_BOOL *pIsStopped
);
```



## Parameters

<dl> <dt>

*pIsStopped* \[out, retval\]
</dt> <dd>

**VARIANT\_TRUE** if the catalog is stopped, otherwise **VARIANT\_FALSE**.

</dd> </dl>

## Return value

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                           |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                 |
| End of client support<br/>    | Windows 7<br/>                                                                 |
| End of server support<br/>    | Windows Server 2008 R2<br/>                                                    |
| DLL<br/>                      | <dl> <dt>Ciodm.dll</dt> </dl> |



## See also

<dl> <dt>

[**ICatAdm**](icatadm.md)
</dt> </dl>

 

 



