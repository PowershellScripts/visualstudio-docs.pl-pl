---
title: IDebugEngine3::SetJustMyCodeState | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugEngine3::SetJustMyCodeState
helpviewer_keywords:
- IDebugEngine3::SetJustMyCodeState
ms.assetid: 8ec17fbf-df93-424a-b2ed-fd1e5ee51256
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ffad3e6be4d81e19bd6f707bd30c744904217ba5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49928974"
---
# <a name="idebugengine3setjustmycodestate"></a>IDebugEngine3::SetJustMyCodeState
Ta metoda informuje aparat debugowania o stan JustMyCode.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT SetJustMyCodeState(  
   BOOL           fUpdate,  
   DWORD          dwModules,  
   JMC_CODE_SPEC* rgJMCSpec  
);  
```  
  
```csharp  
int SetJustMyCodeState(  
   int             fUpdate,   
   uint            dwModules,   
   JMC_CODE_SPEC[] rgJMCSpec  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `fUpdate`  
 [in] Wartość różną od zera (`TRUE`) aby zaktualizować bieżące informacje, od zera (`FALSE`) można zresetować wszystkie informacje (bez uwzględnienia niczego ustawione wcześniej).  
  
 `dwModules`  
 [in] Liczba struktur informacji w `rgJMCSpec.`  
  
 `rgJMCSpec`  
 [in] Tablica [JMC_CODE_SPEC](../../../extensibility/debugger/reference/jmc-code-spec.md) struktury do użycia.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 JustMyCode to pojęcie debugowania tylko kodu, który należy do użytkownika i ignoruje wszelkie kodu pośredniego, takich jak systemu kodu — nawet jeśli kod źródłowy jest dostępny dla tego kodu systemowego.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)   
 [JMC_CODE_SPEC](../../../extensibility/debugger/reference/jmc-code-spec.md)