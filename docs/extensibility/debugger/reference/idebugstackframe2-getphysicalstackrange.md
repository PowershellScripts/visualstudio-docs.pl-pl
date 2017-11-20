---
title: IDebugStackFrame2::GetPhysicalStackRange | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugStackFrame2::GetPhysicalStackRange
helpviewer_keywords: IDebugStackFrame2::GetPhysicalStackRange
ms.assetid: 2f6992e2-ac1c-433f-83b7-a7f83a4ce63d
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a2b57cc7b5959f82b5f02c4939d6645c30c1c706
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugstackframe2getphysicalstackrange"></a>IDebugStackFrame2::GetPhysicalStackRange
Pobiera reprezentację maszyny zależne od zakresu adresów fizycznych skojarzonych z ramki stosu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetPhysicalStackRange (   
   UINT64* paddrMin,  
   UINT64* paddrMax  
);  
```  
  
```csharp  
int GetPhysicalStackRange (   
   out ulong paddrMin,  
   out ulong paddrMax  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `paddrMin`  
 [out] Zwraca adres fizyczny najniższy skojarzone z tą ramką stosu.  
  
 `paddrMax`  
 [out] Zwraca adres fizyczny najwyższy skojarzone z tą ramką stosu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Informacje zwracane przez tę metodę jest używane przez menedżera sesji debugowania (SDM) do sortowania ramki stosu.  
  
 Zakłada się, że stos wywołań rozwoju, oznacza to, dodania nowej ramki stosu w coraz niższych adresów pamięci. Architektura środowiska wykonawczego podać zakresy stosu fizycznych, które odpowiada to założenie.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)