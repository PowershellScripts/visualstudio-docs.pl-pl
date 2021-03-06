---
title: IDebugEngine2::CreatePendingBreakpoint | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugEngine2::CreatePendingBreakpoint
helpviewer_keywords:
- IDebugEngine2::CreatePendingBreakpoint
ms.assetid: 92e85b90-a931-48d9-89a7-a6edcb83ae5a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d711b119e88e9996df19862f9a6779f285ebe4f8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49907017"
---
# <a name="idebugengine2creatependingbreakpoint"></a>IDebugEngine2::CreatePendingBreakpoint
Tworzy oczekujący punkt przerwania w aparacie debugowania (DE).  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT CreatePendingBreakpoint(   
   IDebugBreakpointRequest2*  pBPRequest,  
   IDebugPendingBreakpoint2** ppPendingBP  
);  
```  
  
```csharp  
int CreatePendingBreakpoint(   
   IDebugBreakpointRequest2     pBPRequest,  
   out IDebugPendingBreakpoint2 ppPendingBP  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pBPRequest`  
 [in] [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md) obiekt, który opisuje oczekujący punkt przerwania, aby utworzyć.  
  
 `ppPendingBP`  
 [out] Zwraca [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) obiekt, który reprezentuje oczekujący punkt przerwania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwykle zwraca `E_FAIL` Jeśli `pBPRequest` parametru jest niezgodny z dowolnego języka, obsługiwane przez DE, jeśli `pBPRequest` parametru jest nieprawidłowa lub niekompletna.  
  
## <a name="remarks"></a>Uwagi  
 Oczekujący punkt przerwania jest zasadniczo zbiorem wszystkie informacje potrzebne, aby powiązać punkt przerwania z kodu. Oczekujący punkt przerwania, zwrócone w wyniku tej metody nie jest powiązany z kodu do czasu [powiązać](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) metoda jest wywoływana.  
  
 Dla wszystkich oczekujących punktów przerwania zestawów użytkownika, Menedżer debugowania sesji (SDM) wywołuje tę metodę w każdym DE dołączone. Jest DE, aby sprawdzić, czy punkt przerwania jest prawidłowa dla programów uruchomionych w tym DE.  
  
 Gdy użytkownik ustawia punkt przerwania w wierszu kodu, DE jest bezpłatne powiązać punkt przerwania do najbliższego wiersza w dokumencie, który odnosi się do tego kodu. Dzięki temu użytkownik może ustawić punkt przerwania w pierwszym wierszu instrukcję wiele wierszy, ale powiązać go z ostatniego wiersza (w którym przypisać cały kod w informacjach debugowania).  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak zaimplementować tę metodę dla prostego `CProgram` obiektu. Implementacja DE `IDebugEngine2::CreatePendingBreakpoint` można następnie przesyła wszystkie wywołania do tej implementacji metody w każdym programie.  
  
```  
HRESULT CProgram::CreatePendingBreakpoint(IDebugBreakpointRequest2* pBPRequest, IDebugPendingBreakpoint2** ppPendingBP)     
{    
  
   // Create and initialize the CPendingBreakpoint object.  
   CComObject<CPendingBreakpoint> *pPending;    
   CComObject<CPendingBreakpoint>::CreateInstance(&pPending);    
   pPending->Initialize(pBPRequest, m_pInterp, m_pCallback, m_pEngine);    
   return pPending->QueryInterface(ppPendingBP);    
}    
```  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [powiązania](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)   
 [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md)   
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)