---
title: IDebugProgram2::Step | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::Step
helpviewer_keywords:
- IDebugProgram2::Step
ms.assetid: e4c2ffce-9810-4088-8162-eac9ef04f2a9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 489a641e0f42f6e8e1720929775d8da3df08eeb8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948346"
---
# <a name="idebugprogram2step"></a>IDebugProgram2::Step
Wykonuje krok.  
  
> [!NOTE]
>  Ta metoda jest przestarzała. Użyj [kroku](../../../extensibility/debugger/reference/idebugprocess3-step.md) metody zamiast tego.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Step(   
   IDebugThread2*  pThread,  
   STEPKIND        sk,  
   STEPUNIT        step  
);  
```  
  
```csharp  
int Step(   
   IDebugThread2  pThread,  
   enum_STEPKIND  sk,  
   enum_STEPUNIT  step  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pThread`  
 [in] [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) obiekt, który reprezentuje wątek jest zmieniana.  
  
 `sk`  
 [in] Wartość z zakresu od [STEPKIND](../../../extensibility/debugger/reference/stepkind.md) wyliczenie, które określa rodzaj kroku.  
  
 `step`  
 [in] Wartość z zakresu od [STEPUNIT](../../../extensibility/debugger/reference/stepunit.md) wyliczenie, które określa jednostki kroku (na przykład za pomocą instrukcji lub instrukcji).  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 W przypadku synchronizacji wątków ani komunikacji między wątkami, inne wątki w programie należy uruchomić, gdy przechodzenie krok po kroku określonego wątku.  
  
> [!WARNING]
>  Nie wysyłaj zdarzeń zatrzymywania lub natychmiastowego zdarzenia (synchroniczne) w celu [zdarzeń](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) podczas obsługi tego wywołania; w przeciwnym razie debuger może się zawiesić.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)