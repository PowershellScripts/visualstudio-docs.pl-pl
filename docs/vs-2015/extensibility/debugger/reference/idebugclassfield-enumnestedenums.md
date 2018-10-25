---
title: IDebugClassField::EnumNestedEnums | Dokumentacja firmy Microsoft
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
- IDebugClassField::EnumNestedEnums
helpviewer_keywords:
- IDebugClassField::EnumNestedEnums method
ms.assetid: 90fd0cef-9145-4de6-91d4-6c881df39d6e
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 88447e2006a6bb27cdd4fe92b9ace6389a95430e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49868004"
---
# <a name="idebugclassfieldenumnestedenums"></a>IDebugClassField::EnumNestedEnums
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Tworzy moduł wyliczający dla zagnieżdżonych moduły wyliczające tej klasy.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT EnumNestedEnums(   
   IEnumDebugFields** ppEnum  
);  
```  
  
```csharp  
int EnumNestedEnums(  
   out IEnumDebugFields ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnum`  
 [out] Zwraca [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) obiekt reprezentujący listę zagnieżdżonych wyliczenia. Zwraca wartość null, jeśli nie ma żadnych zagnieżdżonych wyliczenia.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca wartość S_OK lub zwraca wartość S_FALSE, jeśli nie ma żadnych zagnieżdżonych modułów wyliczających. W przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Każdy element wyliczenia jest [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md) Obiekt opisujący zagnieżdżonych wyliczenia.  
  
 Wyliczenie zadeklarowane wewnątrz klasy jest traktowany jako zagnieżdżonych wyliczenia. Na przykład biorąc pod uwagę:  
  
```  
class RootClass {  
   enum NestedEnum { EnumValue = 0 }  
};  
```  
  
 `EnumNestedEnums` Zwróci metoda [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) obiektu, który zawiera jeden [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md) obiekt, który reprezentuje `NestedEnum` wyliczenia.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)   
 [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)

