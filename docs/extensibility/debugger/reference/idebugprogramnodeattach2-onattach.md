---
title: IDebugProgramNodeAttach2::OnAttach | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProgramNodeAttach2::OnAttach
helpviewer_keywords:
- IDebugProgramNodeAttach2::OnAttach
ms.assetid: 5fe52761-a508-4ab5-abdb-334fb6590334
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c30ad0216944ec7c5c707b17df585a689a42b396
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49936143"
---
# <a name="idebugprogramnodeattach2onattach"></a>IDebugProgramNodeAttach2::OnAttach
Dołącza do skojarzonego programu lub procesu dołączania do odracza [Dołącz](../../../extensibility/debugger/reference/idebugengine2-attach.md) metody.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT OnAttach(  
   [in] REFGUID guidProgramId  
);  
```  
  
```csharp  
int OnAttach(  
   ref Guid guidProgramId  
};  
```  
  
#### <a name="parameters"></a>Parametry  
 `guidProgramId`  
 [in] `GUID` można przypisać do skojarzonego programu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`. Zwraca `S_FALSE` Jeśli [Dołącz](../../../extensibility/debugger/reference/idebugengine2-attach.md) nie powinna być wywoływana metoda. W przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest wywoływana podczas procesu dołączania przed [Dołącz](../../../extensibility/debugger/reference/idebugengine2-attach.md) metoda jest wywoływana. `OnAttach` Metodę można wykonać sam proces attach (w którym to przypadku ta metoda zwraca `S_FALSE`) lub Odrocz procesu dołączania do `IDebugEngine2::Attach` — metoda ( `OnAttach` metoda zwraca `S_OK`). W obu przypadkach `OnAttach` metody można ustawić `GUID` programu debugowania do danego `GUID`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md)   
 [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)