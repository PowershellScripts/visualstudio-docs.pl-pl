---
title: IDebugBreakpointRequest2::GetLocationType | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugBreakpointRequest2::GetLocationType
helpviewer_keywords:
- IDebugBreakpointRequest2::GetLocationType
ms.assetid: b6d14c59-d3aa-48ff-8278-f6b5bba9c2f3
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 70189d61752643d78c545a5d33106a4638961c1b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49936241"
---
# <a name="idebugbreakpointrequest2getlocationtype"></a>IDebugBreakpointRequest2::GetLocationType
Pobiera typ lokalizacji punktu przerwania tego żądania punktu przerwania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetLocationType(   
   BP_LOCATION_TYPE* pBPLocationType  
);  
```  
  
```csharp  
int GetLocationType(   
   out enum_BP_LOCATION_TYPE pBPLocationType  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pBPLocationType`  
 [out] Zwraca wartość z zakresu od [BP_LOCATION_TYPE](../../../extensibility/debugger/reference/bp-location-type.md) wyliczenie, opisująca lokalizację tego żądania punktu przerwania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwraca `E_FAIL` Jeśli `bpLocation` pola w skojarzonej [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) struktura jest nieprawidłowa.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak zaimplementować tę metodę dla prostego `CDebugBreakpointRequest` obiekt ujawniający[IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md) interfejsu.  
  
```  
HRESULT CDebugBreakpointRequest::GetLocationType(BP_LOCATION_TYPE* pBPLocationType)    
{    
   HRESULT hr;    
  
   if (pBPLocationType)    
   {    
      // Set default BP_LOCATION_TYPE.    
      *pBPLocationType = BPLT_NONE;    
  
      // Check if the BPREQI_BPLOCATION flag is set in BPREQI_FIELDS.    
      if (IsFlagSet(m_bpRequestInfo.dwFields, BPREQI_BPLOCATION))    
      {    
         // Get the new BP_LOCATION_TYPE.    
         *pBPLocationType = m_bpRequestInfo.bpLocation.bpLocationType;    
         hr = S_OK;    
      }    
      else    
      {    
         hr = E_FAIL;    
      }    
   }    
   else    
   {    
      hr = E_INVALIDARG;    
   }    
  
   return hr;    
}    
```  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md)   
 [BP_LOCATION_TYPE](../../../extensibility/debugger/reference/bp-location-type.md)   
 [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)   
 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)