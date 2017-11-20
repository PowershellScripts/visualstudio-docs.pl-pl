---
title: IDebugThread2::GetName | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugThread2::GetName
helpviewer_keywords: IDebugThread2::GetName
ms.assetid: eec54b8f-4a0e-4919-b0f9-81d4bd1e0b6f
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1c608c01b788c88385814fced4fae99d267e96f4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugthread2getname"></a>IDebugThread2::GetName
Pobiera nazwę wątku.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetName (   
   BSTR* pbstrName  
);  
```  
  
```csharp  
int GetName (   
   out string pbstrName  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pbstrName`  
 [out] Zwraca nazwę wątku.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Pobrana nazwa jest zawsze nazwę, która może być wyświetlana i tej nazwy w tym artykule opisano wątku. Nazwa wątku może pochodzić z architektury środowiska wykonawczego, że obsługuje o nazwie wątków lub może być nazwą pochodnymi aparatu debugowania. Alternatywnie można ustawić nazwę wątku przez wywołanie do [setthreadname —](../../../extensibility/debugger/reference/idebugthread2-setthreadname.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [Setthreadname —](../../../extensibility/debugger/reference/idebugthread2-setthreadname.md)