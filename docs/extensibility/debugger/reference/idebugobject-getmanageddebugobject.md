---
title: IDebugObject::GetManagedDebugObject | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugObject::GetManagedDebugObject
helpviewer_keywords: IDebugObject::GetManagedDebugObject method
ms.assetid: cb89692e-7657-47ff-846d-311943521951
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a01823a2409b15ba101ad4b55d5584e385872574
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugobjectgetmanageddebugobject"></a>IDebugObject::GetManagedDebugObject
Tworzy kopię obiektu zarządzanego w przestrzeni adresowej aparat debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetManagedDebugObject(   
   IDebugManagedObject** ppObject  
);  
```  
  
```csharp  
int GetManagedDebugObject(  
   out IDebugManagedObject ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppObject`  
 [out] Zwraca [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md) obiekt reprezentujący nowo utworzony obiekt zarządzany.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu. Zwraca E_FAIL, jeśli [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nie reprezentuje wystąpienie klasy zarządzanej wartość.  
  
## <a name="remarks"></a>Uwagi  
 To [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) obiektu musi reprezentować wartość zarządzanego wystąpienia klasy, takich jak `System.Decimal` wystąpienia. Dzięki użyciu kopię lokalną obciążenie związane z wywołaniem [Evaluate](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md) wyeliminowania.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)   
 [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)