---
title: IEnumDebugPrograms2::Next | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IEnumDebugPrograms2::Next
helpviewer_keywords:
- IEnumDebugPrograms2::Next
ms.assetid: 9120e263-e97c-4a40-ab2c-e9264ce3d6c4
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4b4c835c4d80ede94751bf2265d0ced318748216
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49925230"
---
# <a name="ienumdebugprograms2next"></a>IEnumDebugPrograms2::Next
Zwraca następny zestaw elementów z wyliczenia.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Next(  
   ULONG            celt,  
   IDebugProgram2** rgelt,  
   ULONG*           pceltFetched  
);  
```  
  
```csharp  
int Next(  
   uint             celt,  
   IDebugProgram2[] rgelt,  
   ref uint         pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `celt`  
 [in] Liczba elementów do pobrania. Również określa maksymalny rozmiar `rgelt` tablicy.  
  
 `rgelt`  
 [out w] Tablica [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) elementami do wypełnienia.  
  
 `pceltFetched`  
 [out] Zwraca liczbę elementów, w rzeczywistości są zwracane w `rgelt`.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`. Zwraca `S_FALSE` Jeśli mniej niż żądana liczba elementów, które mogą być zwracane; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)