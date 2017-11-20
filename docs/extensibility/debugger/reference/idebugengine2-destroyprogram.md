---
title: IDebugEngine2::DestroyProgram | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugEngine2::DestroyProgram
helpviewer_keywords: IDebugEngine2::DestroyProgram
ms.assetid: 0c9e2698-c70f-4770-a7bb-39650e9c3a1f
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d7efe7c8c4d917e6dd1868625ca1d80996176acb
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugengine2destroyprogram"></a>IDebugEngine2::DestroyProgram
Informuje o aparat debugowania (DE) nietypowo zakończone określonego programu, a DE należy wyczyścić wszystkie odwołania do programu i wysyłania program zniszcz zdarzeń.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT DestroyProgram(   
   IDebugProgram2* pProgram  
);  
```  
  
```cpp  
int DestroyProgram(   
   IDebugProgram2 pProgram  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pProgram`  
 [in] [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) obiekt, który reprezentuje program, który został zakończony nietypowo.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Po ta metoda jest wywoływana, DE następnie wysyła [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) zdarzeń do Menedżera debugowania sesji (SDM).  
  
 Ta metoda nie jest zaimplementowana (zwraca `E_NOTIMPL`), gdy DE działa w tym samym procesie jako debugowany program. Ta metoda jest zaimplementowana tylko wtedy, gdy DE działa w ten sam proces jako SDM.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)