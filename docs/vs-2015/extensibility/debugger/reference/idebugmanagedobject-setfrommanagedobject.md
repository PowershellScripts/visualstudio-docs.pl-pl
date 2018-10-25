---
title: IDebugManagedObject::SetFromManagedObject | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugManagedObject::SetFromManagedObject
helpviewer_keywords:
- IDebugManagedObject::SetFromManagedObject method
ms.assetid: 8700ee8d-2704-4580-bccc-046837a24edd
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 89ebc236a2ffa2ea8d2fb2c1bfc71bd33ad4754b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49869525"
---
# <a name="idebugmanagedobjectsetfrommanagedobject"></a>IDebugManagedObject::SetFromManagedObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ustawia wartość wystąpienia obiektu klasy wartości z instancji klasy wartości podać jako parametr.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT SetFromManagedObject(   
   IUnknown* pManagedObject  
);  
```  
  
```csharp  
int SetFromManagedObject(  
   object pManagedObject  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pManagedObject`  
 [in] Interfejs, który reprezentuje zarządzanego obiektu zawierającego nowe wartości.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda służy do zmiany obiektu zarządzanego, reprezentowane przez [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md) obiektu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)

