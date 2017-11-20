---
title: IDebugBinder3::GetTypeArguments | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugBinder3::GetTypeArguments
helpviewer_keywords: IDebugBinder3::GetTypeArguments method
ms.assetid: fa0c37a7-327f-463e-9a9d-bb3f534584cb
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7aff11599f00ad417915c4cb4f4e6ad907b5660d
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugbinder3gettypearguments"></a>IDebugBinder3::GetTypeArguments
Ta metoda pobiera listę typów argumentu skojarzone z tym obiektem.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetTypeArguments(  
   UINT          skip,  
   UINT          count,  
   IDebugField** ppFields,  
   UINT*         pFetched  
);  
```  
  
```csharp  
int GetTypeArguments(  
   uint          skip,  
   uint          count,  
   IDebugField[] ppFields,  
   out uint      pFetched  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `skip`  
 [in] Numer pola, aby pominąć przed pobraniem typy argumentów.  
  
 `count`  
 [in] Liczba pól argument do zwrócenia (również określa rozmiar `ppFields` tablicy).  
  
 `ppFields`  
 [w, out] Tablica pola, które są wypełniane przy powrocie z tej metody.  
  
 `pFetched`  
 [out] \(opcjonalne) Liczba argumentów typu pola faktycznie zwracane.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Liczba typów argumentów można uzyskać z wcześniej [GetTypeArgumentCount](../../../extensibility/debugger/reference/idebugbinder3-gettypeargumentcount.md).  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)   
 [GetTypeArgumentCount](../../../extensibility/debugger/reference/idebugbinder3-gettypeargumentcount.md)