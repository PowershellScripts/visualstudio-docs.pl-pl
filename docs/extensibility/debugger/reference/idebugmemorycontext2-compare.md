---
title: IDebugMemoryContext2::Compare | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugMemoryContext2::Compare
helpviewer_keywords:
- IDebugMemoryContext2::Compare method
- Compare method
ms.assetid: c51b5128-848e-4d8e-b2e9-1161339763c3
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 5be5c6dccecc8191030482c282033aa6159f2022
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49873906"
---
# <a name="idebugmemorycontext2compare"></a>IDebugMemoryContext2::Compare
Porównuje kontekstu pamięci dla każdego kontekstu w podanej tablicy w sposób wskazany przez porównanie flag, zwraca indeks pierwszego kontekst, który jest zgodny.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Compare(   
   CONTEXT_COMPARE        compare,  
   IDebugMemoryContext2** rgpMemoryContextSet,  
   DWORD                  dwMemoryContextSetLen,  
   DWORD*                 pdwMemoryContext  
);  
```  
  
```csharp  
int Compare(  
   enum_CONTEXT_COMPARE   compare,   
   IDebugMemoryContext2[] rgpMemoryContextSet,   
   uint                   dwMemoryContextSetLen,   
   out uint               pdwMemoryContext  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `compare`  
 [in] Wartość z zakresu od [CONTEXT_COMPARE](../../../extensibility/debugger/reference/context-compare.md) wyliczenie, który określa typ porównania.  
  
 `rgpMemoryContextSet`  
 [in] Tablica odniesień do [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) obiektów, które ma zostać wykonane porównanie.  
  
 `dwMemoryContextSetLen`  
 [in] Liczbę kontekstów w `rgpMemoryContextSet` tablicy.  
  
 `pdwMemoryContext`  
 [out] Zwraca indeks pierwszego kontekst pamięci, który spełnia porównanie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwraca `E_COMPARE_CANNOT_COMPARE` Jeśli nie można porównać dwóch kontekstów.  
  
## <a name="remarks"></a>Uwagi  
 Aparat debugowania (DE) nie ma do obsługi wszystkich rodzajów porównań, ale musi obsługiwać co najmniej `CONTEXT_EQUAL`, `CONTEXT_LESS_THAN`, `CONTEXT_GREATER_THAN` i `CONTEXT_SAME_SCOPE`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)   
 [CONTEXT_COMPARE](../../../extensibility/debugger/reference/context-compare.md)