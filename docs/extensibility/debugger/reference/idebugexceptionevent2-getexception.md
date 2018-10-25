---
title: IDebugExceptionEvent2::GetException | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugExceptionEvent2::GetException
helpviewer_keywords:
- IDebugExceptionEvent2::GetException
ms.assetid: 7c98f41d-322b-4e72-a514-cbd4823eb70d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: b4c62a12c54a716a02146190b91f1f95365333b9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49917131"
---
# <a name="idebugexceptionevent2getexception"></a>IDebugExceptionEvent2::GetException
Pobiera szczegółowy opis wyjątku, która wywołała zdarzenie.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetException(   
   EXCEPTION_INFO* pExceptionInfo  
);  
```  
  
```csharp  
int GetException(   
   EXCEPTION_INFO[] pExceptionInfo  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pExceptionInfo`  
 [out w] [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md) strukturę, która jest wypełniane opis wyjątku.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 [Tylko w języku C++] Obiekt wywołujący jest odpowiedzialny za zwalnianie wszystkie ciągi w [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md) struktury, a także udostępnia [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) obiektu w strukturze.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)   
 [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)