---
title: IDebugClassField::GetEnclosingClass | Dokumentacja firmy Microsoft
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
- IDebugClassField::GetEnclosingClass
helpviewer_keywords:
- IDebugClassField::GetEnclosingClass method
ms.assetid: a0c12e3c-9ea0-4dfb-9e45-8cea18725022
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 69c9359fe8d9f337a09e0ab3fae4f92b0fc4c264
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49924748"
---
# <a name="idebugclassfieldgetenclosingclass"></a>IDebugClassField::GetEnclosingClass
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Pobiera klasę, która otacza tej klasy.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT GetEnclosingClass(   
   IDebugClassField** ppClassField  
);  
```  
  
```csharp  
int GetEnclosingClass(  
   out IDebugClassField ppClassField  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppClassField`  
 [out] Zwraca [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) obiekt reprezentujący otaczającej klasy. Zwraca wartość null, jeśli nie otaczającej klasy.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Jeśli klasa reprezentowany przez ten [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) obiekt jest klasy zagnieżdżonej, a następnie `ppClassField` parametr zwraca `IDebugClassField` obiekt reprezentujący otaczającej klasy. Na przykład biorąc pod uwagę tę definicję klasy:  
  
```  
class RootClass {  
   class NestedClass { }  
};  
```  
  
 Wywoływanie `GetEnclosingClass` metody `IDebugClassField` obiekt reprezentujący `NestedClass` klasy zwraca `IDebugClassField` obiekt reprezentujący klasę `RootClass`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)

