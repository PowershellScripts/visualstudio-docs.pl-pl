---
title: IDebugProperty2::GetParent | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugProperty2::GetParent
helpviewer_keywords:
- IDebugProperty2::GetParent
ms.assetid: 58780469-fe25-4d84-9187-67940ca0767f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 92e3ffde948d7f36e02a4b76086e7b4cee290fa1
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49864143"
---
# <a name="idebugproperty2getparent"></a>IDebugProperty2::GetParent
Pobiera właściwość nadrzędna właściwości.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetParent (   
   IDebugProperty2** ppParent  
);  
```  
  
```csharp  
int GetParent (   
   out IDebugProperty2 ppParent  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppParent`  
 [out] Zwraca [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) obiekt, który reprezentuje element nadrzędny właściwości.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwraca `S_GETPARENT_NO_PARENT` Jeśli brak elementu nadrzędnego.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)