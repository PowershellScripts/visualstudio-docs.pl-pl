---
title: IDebugPointerField::GetDereferencedField | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugPointerField::GetDereferencedField
helpviewer_keywords:
- IDebugPointerField::GetDereferencedField method
ms.assetid: 8de988ab-cd79-4287-be72-3c900f2fe407
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 685499cae556a50a5e98e8fe32e8104098cc79e6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49933251"
---
# <a name="idebugpointerfieldgetdereferencedfield"></a>IDebugPointerField::GetDereferencedField
Ta metoda zwraca typ obiektu, na który wskazuje ten obiekt wskaźnika.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetDereferencedField(  
   IDebugField** ppField  
);  
```  
  
```csharp  
int GetDereferencedField(  
   out IDebugField ppField  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppField`  
 [out] Zwraca [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) opisujące typ obiektu docelowego.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Jeśli na przykład [IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md) obiektu wskazuje na liczbę całkowitą, [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) typu zwracanego przez tę metodę zawiera opis tego typu Liczba całkowita.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)