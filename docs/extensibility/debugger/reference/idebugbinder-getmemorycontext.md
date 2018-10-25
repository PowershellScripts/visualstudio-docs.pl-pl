---
title: IDebugBinder::GetMemoryContext | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugBinder::GetMemoryContext
helpviewer_keywords:
- IDebugBinder::GetMemoryContext method
ms.assetid: 801c5b60-acff-4822-b23d-e9c7bbca8a0f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a94098a6645ef353ff3e18b17911c05d495fe8ae
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49905444"
---
# <a name="idebugbindergetmemorycontext"></a>IDebugBinder::GetMemoryContext
Ta metoda konwertuje lokalizacji obiektu lub adres pamięci do kontekstu pamięci.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetMemoryContext(   
   IDebugField*           pField,  
   DWORD                  dwConstant,  
   IDebugMemoryContext2** ppMemCxt  
);  
```  
  
```csharp  
int GetMemoryContext(  
   IDebugField              pField,   
   uint                     dwConstant,   
   out IDebugMemoryContext2 ppMemCxt  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pField`  
 [in] [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) opisujący obiekt do zlokalizowania. Jeśli `NULL`, następnie za pomocą `dwConstant` zamiast tego.  
  
 `dwConstant`  
 [in] Adres pamięci stałych, takich jak 0x5000.  
  
 `ppMemCxt`  
 [out] Zwraca [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) interfejs, który reprezentuje adres obiektu lub adresu w pamięci.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)   
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)