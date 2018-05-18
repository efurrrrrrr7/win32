---
title: INapSystemHealthAgentRequest GetSoHResponse method
description: Is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: '60319256-d5c2-46cc-a59b-f81732e21a7f'
keywords: ["GetSoHResponse method NAP", "GetSoHResponse method NAP , INapSystemHealthAgentRequest interface", "INapSystemHealthAgentRequest interface NAP , GetSoHResponse method"]
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
---

# INapSystemHealthAgentRequest::GetSoHResponse method

> [!Note]  
> The Network Access Protection platform is not available starting with Windows�10

�

The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## Syntax


```C++
HRESULT GetSoHResponse(
  [out]�SoHResponse **sohResponse,
  [out]�UINT8 ������*flags
);
```



## Parameters

<dl> <dt>

*sohResponse* \[out\]
</dt> <dd>

A pointer to a pointer to a [**SoHResponse**](soh-struct.md) packet.

</dd> <dt>

*flags* \[out\]
</dt> <dd>

A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.



| Possible Values                                                                                                                                                          | Meaning                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | The SHA is expected to perform the fixup based on the response. If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](soh-struct.md) indicates that it is unhealthy.<br/> |



�

</dd> </dl>

## Return value

Other COM-specific error codes also may be returned.



| Return code                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S\_OK** </dt> </dl>           | Operation succeeded.<br/>                                    |
| <dl> <dt>**E\_ACCESSDENIED** </dt> </dl> | Permissions error, access denied.<br/>                       |
| <dl> <dt>**E\_OUTOFMEMORY** </dt> </dl>  | System resource limit, could not perform the operation.<br/> |



�

## Requirements



|                                     |                                                                                                     |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                                      |
| Minimum supported server<br/> | Windows Server�2008 \[desktop apps only\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## See also

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

�

�




