---
title: Iteration AddMetricValue method
description: Creates and adds a MetricValue whose value is a DOUBLE.
ms.assetid: 430C46D9-9EAB-451D-ABB8-3FB1CD6DE1D1
keywords:
- AddMetricValue method Access Execution Engine
- AddMetricValue method Access Execution Engine , Iteration interface
- Iteration interface Access Execution Engine , AddMetricValue method
topic_type:
- apiref
api_name:
- Iteration.AddMetricValue
api_location:
- AxeCore.dll
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Iteration::AddMetricValue method

Creates and adds a [**MetricValue**](metricvalue-struct.md) whose value is a **DOUBLE**.

## Syntax


```C++
virtual HRESULT AddMetricValue(
  [in]  LPCWSTR     programmaticName,
  [in]  DOUBLE      value,
  [out] MetricValue **metricValue
) = 0;
```



## Parameters

<dl> <dt>

*programmaticName* \[in\]
</dt> <dd>

The programmatic name.

</dd> <dt>

*value* \[in\]
</dt> <dd>

The value.

</dd> <dt>

*metricValue* \[out\]
</dt> <dd>

The **MetricValue** that this method creates.

</dd> </dl>

## Return value

If the function succeeds, it returns **S\_OK**. If it fails, it returns an error value.

## Remarks

The programmatic name is the value of element **MetricValue/ProgrammaticName**.

The value is the value of element **MetricValue/Value**.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                              |
| Minimum supported server<br/> | Windows Server 2008 R2 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>AxeRuntime.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AxeCore.dll</dt> </dl>  |



## See also

<dl> <dt>

[**Iteration**](iteration-struct.md)
</dt> </dl>

 

 




