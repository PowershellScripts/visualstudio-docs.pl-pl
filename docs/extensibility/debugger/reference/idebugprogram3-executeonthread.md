---
title: IDebugProgram3::ExecuteOnThread | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- IDebugProgram3::ExecuteOnThread
ms.assetid: 2f5211e3-7a3f-47bf-9595-dfc8b4895d0d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: afca4a97380d010897ca1dfb7c6229f3f1897ef9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49865950"
---
# <a name="idebugprogram3executeonthread"></a>IDebugProgram3::ExecuteOnThread
Wykonuje program debugera. Wątek jest zwracany do przedstawienia informacji debugera, na który wątek użytkownika jest wyświetlana podczas wykonywania programu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT ExecuteOnThread(  
   [in] IDebugThread2* pThread)  
```  
  
```csharp  
int ExecuteOnThread(  
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pThread`  
 [in] [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) obiektu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Istnieją trzy różne sposoby wznowić wykonywanie po zatrzymaniu debugera:  
  
- Wykonaj: Anulowanie wszelkich w poprzednim kroku, a następnie uruchom aż do następnego punktu przerwania i tak dalej.  
  
- Krok Anulować stary którykolwiek z kroków i uruchamianie aż do zakończenia nowego kroku.  
  
- Kontynuuj: Uruchom ponownie i pozostawianie aktywnej stare którykolwiek z kroków.  
  
  Wątek jest przekazywany do `ExecuteOnThread` jest przydatne w przypadku podejmowania decyzji, który krok, aby anulować. Jeśli nie znasz wątek systemu wykonaj anuluje wszystkie kroki. Przy zachowaniu wiedzy o wątku wystarczy anulować kroku na aktywnym wątkiem.  
  
## <a name="see-also"></a>Zobacz też  
 [Wykonywanie](../../../extensibility/debugger/reference/idebugprogram2-execute.md)   
 [IDebugProgram3](../../../extensibility/debugger/reference/idebugprogram3.md)