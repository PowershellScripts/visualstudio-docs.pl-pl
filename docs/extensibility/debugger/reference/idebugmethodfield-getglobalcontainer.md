---
title: IDebugMethodField::GetGlobalContainer | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugMethodField::GetGlobalContainer
helpviewer_keywords: IDebugMethodField::GetGlobalContainer method
ms.assetid: 041ac5aa-0b80-4310-b9ae-b88f8e7e0e5f
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ffeb7c7c1abe6e5a816c2d7a67ad6820e0921bc8
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugmethodfieldgetglobalcontainer"></a>IDebugMethodField::GetGlobalContainer
Pobiera kontener globalnej metody.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetGlobalContainer(  
   IDebugClassField** ppClass  
);  
```  
  
```csharp  
int GetGlobalContainer(  
   out IDebugClassField ppClass  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppClass`  
 [out] Zwraca [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) reprezentujący modułu, w którym ta metoda jest zdefiniowany.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Zwrócona [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) obiekt reprezentuje cały moduł i jest obiektem sztuczne, oznacza to, moduł sam nie rzeczywiste klasy ale może być reprezentowany przez `IDebugClassField` obiektu, dzięki czemu różne elementy modułu wyliczone i odnalezione.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)   
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)