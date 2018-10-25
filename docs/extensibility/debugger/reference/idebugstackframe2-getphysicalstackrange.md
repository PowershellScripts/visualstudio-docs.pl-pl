---
title: IDebugStackFrame2::GetPhysicalStackRange | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugStackFrame2::GetPhysicalStackRange
helpviewer_keywords:
- IDebugStackFrame2::GetPhysicalStackRange
ms.assetid: 2f6992e2-ac1c-433f-83b7-a7f83a4ce63d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a1b46dd9993eb8a7611b4d84211016168d609101
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49950384"
---
# <a name="idebugstackframe2getphysicalstackrange"></a>IDebugStackFrame2::GetPhysicalStackRange
Pobiera reprezentację zależnych od maszyny, zakresu adresów fizycznych skojarzonych z ramki stosu.  
  
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
 [out] Zwraca najniższy adres fizyczny skojarzone z tą ramką stosu.  
  
 `paddrMax`  
 [out] Zwraca najwyższy adres fizyczny skojarzone z tą ramką stosu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Informacje zwracane przez tę metodę jest używany przez Menedżer debugowania sesji (SDM) do sortowania ramki stosu.  
  
 Zakłada się, że stos wywołań rośnie, oznacza to, dodania nowej ramki stosu w coraz większym stopniu niższe adresów pamięci. Architektura środowiska wykonawczego, musisz podać zakresy adresów fizycznych stosu, które odpowiadają tym założeń.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)