---
title: IDebugExceptionEvent2::PassToDebuggee | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugExceptionEvent2::PassToDebuggee
helpviewer_keywords:
- IDebugExceptionEvent2::PassToDebuggee
ms.assetid: a20d0f0b-2ca0-4437-bd22-9213c81d2738
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3b1fb575299000e4b9ab894a4700fdf314d17d6c
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49832709"
---
# <a name="idebugexceptionevent2passtodebuggee"></a>IDebugExceptionEvent2::PassToDebuggee
Określa, czy wyjątek powinien zostać przekazany do aktualnie debugowanego po wznowieniu działania wykonywania, czy wyjątek powinien zostać odrzucony.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT PassToDebuggee(  
   BOOL fPass  
);  
```  
  
```csharp  
int PassToDebuggee(  
   int fPass  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `fPass`  
 [in] Wartość różną od zera (`TRUE`) Jeśli wyjątek powinien być przekazywane do debugowanego po wznowieniu działania wykonywania lub zero (`FALSE`) Jeśli wyjątek powinien zostać odrzucony.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Wywołanie tej metody nie faktycznie powoduje żadnego kodu do wykonania w debugowanego programu. Wywołanie jest jedynie można ustawić stanu dla następnego wykonania kodu. Na przykład wywołania [CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) metoda może zwrócić `S_OK` z [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md).`dwState` Ustaw pole `EXCEPTION_STOP_SECOND_CHANCE`.  
  
 IDE może zostać wyświetlony [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md) zdarzenia i wywołania [Kontynuuj](../../../extensibility/debugger/reference/idebugprogram2-continue.md) metody. Aparat debugowania (DE) powinien mieć domyślne zachowanie w celu obsługi sytuacji, gdy `PassToDebuggee` nie jest wywoływana metoda.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)   
 [CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)   
 [Continue](../../../extensibility/debugger/reference/idebugprogram2-continue.md)