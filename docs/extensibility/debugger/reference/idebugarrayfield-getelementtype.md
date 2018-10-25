---
title: IDebugArrayField::GetElementType | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugArrayField::GetElementType
helpviewer_keywords:
- IDebugArrayField::GetElementType method
ms.assetid: c46bf625-0a48-4cbb-8f1f-286356f2c065
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c95457fdc91e4c625cb56aaba58593acf2a64e16
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49821945"
---
# <a name="idebugarrayfieldgetelementtype"></a>IDebugArrayField::GetElementType
Pobiera typ elementu w tablicy.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetElementType(   
   IDebugField** ppType  
);  
```  
  
```csharp  
int GetElementType(  
   out IDebugField ppType  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppType`  
 [out] Zwraca [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) obiekt, który opisuje typ elementu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 [IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md) obiektu przyjęto założenie, że wszystkie elementy tablicy są tego samego typu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)