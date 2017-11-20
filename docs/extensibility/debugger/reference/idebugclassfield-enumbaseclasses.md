---
title: IDebugClassField::EnumBaseClasses | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugClassField::EnumBaseClasses
helpviewer_keywords: IDebugClassField::EnumBaseClasses method
ms.assetid: 78749674-ef75-46d3-a1f4-ff33afd90e32
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6c86f631d08fa3a3d7a43b1da2d6555370257c6b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugclassfieldenumbaseclasses"></a>IDebugClassField::EnumBaseClasses
Tworzy moduł wyliczający dla klasy podstawowe tej klasy.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT EnumBaseClasses(   
   IEnumDebugFields** ppEnum  
);  
```  
  
```csharp  
int EnumBaseClasses(  
   out IEnumDebugFields ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnum`  
 [out] Zwraca [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) obiekt reprezentujący listę klas podstawowych. Zwraca wartość null, jeśli istnieją nie klas podstawowych.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca wartość S_OK, S_SH_NO_BASE_CLASSES przypadku nie klas podstawowych (i `ppEnum` ustawiona jest wartość null); w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Klasy podstawowe w obiekcie modułu wyliczającego są określone w kolejności od najbardziej bezpośrednim (lub najbardziej pochodnej) klasę podstawową do najbardziej zdalnego klasy podstawowej. Przykładowo podana klasy C++:  
  
```  
class Root { }  
class Level1 : Root { }  
class Level2 : Level1 { }  
class MyClass : Level2 { }  
```  
  
 Wyliczenie zwróci klasy podstawowe w kolejności `Level2`, `Level1`, `Root`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)