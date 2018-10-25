---
title: IDebugDefaultPort2::QueryIsLocal | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugDefaultPort2::QueryIsLocal
helpviewer_keywords:
- IDebugDefaultPort2::QueryIsLocal
ms.assetid: 1a42e774-c6ed-419a-a0e3-cab5778652ca
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 2ed411d632df544d47b376e59bc59b7331d8aa91
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49901810"
---
# <a name="idebugdefaultport2queryislocal"></a>IDebugDefaultPort2::QueryIsLocal
Ta metoda określa, czy ten port jest na komputerze lokalnym.  
  
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
 Zwraca `S_OK` czy ten port jest lokalny (na tym samym komputerze co obiekt wywołujący) lub `S_FALSE` Jeśli port znajduje się na innym komputerze.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)