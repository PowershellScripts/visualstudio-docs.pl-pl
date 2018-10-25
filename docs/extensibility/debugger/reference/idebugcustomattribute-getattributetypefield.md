---
title: IDebugCustomAttribute::GetAttributeTypeField | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugCustomAttribute::GetAttributeTypeField
helpviewer_keywords:
- IDebugCustomAttribute::GetAttributeTypeField
ms.assetid: d6ce26d5-42ba-44c1-8659-0516db5bc82d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e5a01f5c0aeb9d22d0dc07ef9e436e8649c6bd3b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49846333"
---
# <a name="idebugcustomattributegetattributetypefield"></a>IDebugCustomAttribute::GetAttributeTypeField
Pobiera typ klasy atrybutu niestandardowego.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetAttributeTypeField(   
   IDebugClassField** ppCAType  
);  
```  
  
```csharp  
int GetAttributeTypeField(  
   out IDebugClassField ppCAType  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppCAType`  
 [out] Zwraca [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) obiekt, który reprezentuje klasę, którego wystąpienie jest atrybutu niestandardowego.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Atrybut niestandardowy jest zawsze klasy. Ta metoda zapewnia dostęp do [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) obiekt, który opisuje tę klasę.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)   
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)