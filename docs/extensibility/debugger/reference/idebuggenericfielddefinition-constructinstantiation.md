---
title: IDebugGenericFieldDefinition::ConstructInstantiation | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- ConstructInstantiation
- IDebugGenericFieldDefinition::ConstructInstantiation
ms.assetid: ef8ae261-a98b-4dc2-93b3-7c5191818ba2
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: cc2c710e7fbd9a6fef3283f6dc5790707c65d30a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49933056"
---
# <a name="idebuggenericfielddefinitionconstructinstantiation"></a>IDebugGenericFieldDefinition::ConstructInstantiation
Tworzy wystąpienie pola, biorąc pod uwagę tablicę argumentów typu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT ConstructInstantiation(  
   ULONG32       cArgs,  
   IDebugField** ppArgs,  
   IDebugField** ppConstructedField  
);  
```  
  
```csharp  
int ConstructInstantiation(  
   uint            cArgs,  
   IDebugField[]   ppArgs,  
   out IDebugField ppConstructedField  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `cArgs`  
 [in] Liczba argumentów w `ppArgs` tablicy.  
  
 `ppArgs`  
 [in] Tablica, która zawiera argumenty typu. Argumenty typu muszą być zamknięte typy (Ogólne nieogólnego lub w pełni utworzona).  
  
 `ppConstructedField`  
 [out] Zwraca [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) interfejs, który reprezentuje nowe pole.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ograniczenia nie są sprawdzane.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugGenericFieldDefinition](../../../extensibility/debugger/reference/idebuggenericfielddefinition.md)