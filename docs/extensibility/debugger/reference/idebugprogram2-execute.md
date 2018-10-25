---
title: IDebugProgram2::Execute | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::Execute
helpviewer_keywords:
- IDebugProgram2::Execute
ms.assetid: f7205ce8-0ac6-4fcd-b6ec-b720b4fcaccf
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 35a3845911bf9a1ebfd90165b1c6fde45d797696
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49842589"
---
# <a name="idebugprogram2execute"></a>IDebugProgram2::Execute
Nadal uruchomiony ten program w stanie zatrzymania. Jest wyczyszczone wszelkie poprzedni stan wykonania (np. krok), i ponownym wykonaniem uruchamiania programu.  
  
> [!NOTE]
>  Ta metoda jest przestarzała. Użyj [Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md) metody zamiast tego.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Execute(  
   void  
);  
```  
  
```csharp  
int Execute();  
```  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Gdy użytkownik rozpoczyna wykonywanie w stanie zatrzymania wątku przez inny program, ta metoda jest wywoływana dla tego programu. Ta metoda również jest wywoływana, gdy użytkownik wybierze **Start** polecenia **debugowania** menu w środowisku IDE. Implementacja tej metody może być proste co wywołanie metody [Wznów](../../../extensibility/debugger/reference/idebugthread2-resume.md) metody w bieżącym wątku w programie.  
  
> [!WARNING]
>  Nie wysyłaj zdarzeń zatrzymywania lub natychmiastowego zdarzenia (synchroniczne) w celu [zdarzeń](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) podczas obsługi tego wywołania; w przeciwnym razie debuger może się zawiesić.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [Zdarzenia](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)   
 [Resume](../../../extensibility/debugger/reference/idebugthread2-resume.md)