---
title: IDebugThread2::Resume | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugThread2::Resume
helpviewer_keywords:
- IDebugThread2::Resume
ms.assetid: 36aad682-b0b9-40a2-b3fc-f0e61d41cdbc
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f41f26c824a779133a335c0d3d5080373b791d06
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49920992"
---
# <a name="idebugthread2resume"></a>IDebugThread2::Resume
Wznawia wykonanie wątku.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Resume (   
   DWORD *pdwSuspendCount  
);  
```  
  
```csharp  
int Resume (   
   out uint pdwSuspendCount  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pdwSuspendCount`  
 [out] Zwraca wstrzymania liczenia przez operację wznawiania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Każdy wywołanie tej metody zmniejsza wstrzymania liczenia aż do napotkania 0 w tym czasie faktycznie wznowiono wykonywanie. Ten licznik Wstrzymaj jest wyświetlana w **wątków** okna debugowania.  
  
 Dla każdego wywołania tej metody musi być poprzednie wywołanie [Wstrzymaj](../../../extensibility/debugger/reference/idebugthread2-suspend.md) metody. Wstrzymania liczenia Określa, ile razy `IDebugThread2::Suspend` do tej pory została wywołana metoda.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [Suspend](../../../extensibility/debugger/reference/idebugthread2-suspend.md)