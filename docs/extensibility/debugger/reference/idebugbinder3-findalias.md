---
title: IDebugBinder3::FindAlias | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugBinder3::FindAlias
helpviewer_keywords: IDebugBinder3::FindAlias method
ms.assetid: b8333701-2718-4983-8513-0875fb7cb730
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f209829e3b6c76571a53370c11c6d6d7343b088c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugbinder3findalias"></a>IDebugBinder3::FindAlias
Ta metoda lokalizuje alias podanej nazwy. Przeszuka wszystkie aliasy programu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT FindAlias(  
   LPCOLESTR     pcstrName,  
   IDebugAlias** ppAlias  
);  
```  
  
```csharp  
int FindAlias(  
   string          pcstrName,  
   out IDebugAlias ppAlias  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pcstrName`  
 [in] Nazwa aliasu można znaleźć.  
  
 `ppAlias`  
 [out] Znaleziono (jeśli istnieją) alias reprezentowany przez [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md) interfejsu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` (Jeśli nie ma aliasu) lub kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda inicjuje obiekt docelowy, na wartość null przed wywołaniem; następnie testy później w celu ustalenia, czy został znaleziony alias występuje wartość null.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)   
 [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)