---
title: IDebugDefaultPort2::QueryIsLocal | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugDefaultPort2::QueryIsLocal
helpviewer_keywords: IDebugDefaultPort2::QueryIsLocal
ms.assetid: 1a42e774-c6ed-419a-a0e3-cab5778652ca
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b90459eb9dc3a2646bbe1ba5eb9ab25e9a8327b6
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugdefaultport2queryislocal"></a>IDebugDefaultPort2::QueryIsLocal
Ta metoda określa, czy ten port na komputerze lokalnym.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT QueryIsLocal(  
   void  
);  
```  
  
```csharp  
int QueryIsLocal();  
```  
  
## <a name="return-value"></a>Wartość zwracana  
 Zwraca `S_OK` czy ten port jest lokalny (na tym samym komputerze co wywołującego) lub `S_FALSE` Jeśli port jest na innym komputerze.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)