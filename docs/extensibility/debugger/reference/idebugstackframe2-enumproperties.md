---
title: IDebugStackFrame2::EnumProperties | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugStackFrame2::EnumProperties
helpviewer_keywords: IDebugStackFrame2::EnumProperties
ms.assetid: 334bb95e-c7e0-4008-9f06-8c3999e47ee8
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c2679317497568e9f844bcf9503fc0057ca6158c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugstackframe2enumproperties"></a>IDebugStackFrame2::EnumProperties
Tworzy moduł wyliczający dla właściwości skojarzone z ramki stosu, takich jak zmiennych lokalnych.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT EnumProperties (   
   DEBUGPROP_INFO_FLAGS      dwFieldSpec,  
   UINT                      nRadix,  
   REFIID                    refiid,  
   DWORD                     dwTimeout,  
   ULONG*                    pcelt,  
   IEnumDebugPropertyInfo2** ppEnum  
);  
```  
  
```csharp  
int EnumProperties (   
   enum_DEBUGPROP_INFO_FLAGS   dwFieldSpec,  
   uint                        nRadix,  
   ref Guid                    refiid,  
   uint                        dwTimeout,  
   out uint                    pcelt,  
   out IEnumDebugPropertyInfo2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `dwFieldSpec`  
 [in] Kombinacja flag z [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md) wyliczenie określający pola, które w wyliczany [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) struktury mają zostać wypełnione.  
  
 `nRadix`  
 [in] Podstawa ma być używany podczas formatowania wszelkie informacje numeryczne.  
  
 `refiid`  
 [in] Identyfikator GUID używany do wybierania który filtru [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) struktury mają zostać wyliczone, takich jak `guidFilterLocals`.  
  
 `dwTimeout`  
 [in] Maksymalny czas (w milisekundach) oczekiwania przed powrotem z tej metody. Użyj `INFINITE` będzie czekać w nieskończoność.  
  
 `pcelt`  
 [out] Zwraca liczbę właściwości wyliczone. Jest to ten sam co wywołanie [GetCount](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-getcount.md) metody.  
  
 `ppEnum`  
 [out] Zwraca [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md) zawierającego listę właściwości żądanego obiektu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ponieważ ta metoda umożliwia wszystkich wybranych właściwości mają zostać pobrane przy użyciu jednego wywołania, jest szybsza niż sekwencyjnie wywoływania [GetDebugProperty](../../../extensibility/debugger/reference/idebugstackframe2-getdebugproperty.md) i [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md)   
 [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md)   
 [GetCount](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2-getcount.md)   
 [GetDebugProperty](../../../extensibility/debugger/reference/idebugstackframe2-getdebugproperty.md)   
 [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md)