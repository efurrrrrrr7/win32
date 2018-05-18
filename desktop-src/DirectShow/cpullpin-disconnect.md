---
Description: 'The Disconnect method breaks the connection with the output pin.'
ms.assetid: '6e362e32-7b74-4392-b46f-1ab47a30a07b'
title: 'CPullPin.Disconnect method'
---

# CPullPin.Disconnect method

The `Disconnect` method breaks the connection with the output pin.

## Syntax


```C++
HRESULT Disconnect();
```



## Parameters

This method has no parameters.

## Return value

Returns S\_OK.

## Remarks

This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method. Call this method inside your [**IPin::Disconnect**](ipin-disconnect.md) method. (If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CPullPin Class**](cpullpin.md)
</dt> </dl>

�

�



