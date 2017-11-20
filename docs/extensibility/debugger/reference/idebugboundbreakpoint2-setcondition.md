---
title: IDebugBoundBreakpoint2::SetCondition | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugBoundBreakpoint2::SetCondition
helpviewer_keywords:
- SetCondition method
- IDebugBoundBreakpoint2::SetCondition method
ms.assetid: 5d366876-efed-43d0-8ea1-dfdb009cbfac
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5d5d6f04e420ed7268c009467f74c020d429ab2b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugboundbreakpoint2setcondition"></a>IDebugBoundBreakpoint2::SetCondition
Ustawia lub zmienia warunek skojarzony z tym powiązania punktu przerwania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT SetCondition(   
   BP_CONDITION bpCondition  
);  
```  
  
```csharp  
int SetCondition(   
   enum_BP_CONDITION bpCondition  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `bpCondition`  
 [in] Wartość z zakresu od [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) wyliczenie opisujące stan.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwraca `E_BP_DELETED` Jeśli stan obiektu powiązanego punktu przerwania jest równa `BPS_DELETED` (część [BP_STATE](../../../extensibility/debugger/reference/bp-state.md) wyliczenie).  
  
## <a name="remarks"></a>Uwagi  
 Wszelkie warunek, który został wcześniej skojarzony z tego punktu przerwania zostaną utracone.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugBoundBreakpoint2](../../../extensibility/debugger/reference/idebugboundbreakpoint2.md)   
 [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)   
 [BP_STATE](../../../extensibility/debugger/reference/bp-state.md)