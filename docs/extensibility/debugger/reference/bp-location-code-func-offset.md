---
title: BP_LOCATION_CODE_FUNC_OFFSET | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- BP_LOCATION_CODE_FUNC_OFFSET
helpviewer_keywords:
- BP_LOCATION_CODE_FUNC_OFFSET structure
ms.assetid: ab38f7ca-fa01-4cf3-a06c-56cbb7207617
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9a1828a7cea62893ecddec6d28f44ca6475352dd
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49911398"
---
# <a name="bplocationcodefuncoffset"></a>BP_LOCATION_CODE_FUNC_OFFSET
W tym artykule opisano przesunięcia lokalizacji punktu przerwania w funkcji w kodzie.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct _BP_LOCATION_CODE_FUNC_OFFSET {   
   BSTR                     bstrContext;  
   IDebugFunctionPosition2* pFuncPos;  
} BP_LOCATION_CODE_FUNC_OFFSET;  
```  
  
## <a name="members"></a>Elementy członkowskie  
 `bstrContext`  
 Kontekst punktu przerwania, zazwyczaj nazwę metody lub funkcji wyświetlanego w stosie wywołań.  
  
 `pFuncPos`  
 [IDebugFunctionPosition2](../../../extensibility/debugger/reference/idebugfunctionposition2.md) obiekt, który opisuje nazwę funkcji i względnego położenia od samego początku funkcji.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest elementem członkowskim [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) struktur w ramach złożenia.  
  
 `pFuncPos` Członka wskazuje, gdzie można ustawić punktu przerwania funkcji.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)   
 [IDebugFunctionPosition2](../../../extensibility/debugger/reference/idebugfunctionposition2.md)