---
title: IDebugProcess2::EnumThreads | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugProcess2::EnumThreads
helpviewer_keywords: IDebugProcess2::EnumThreads
ms.assetid: 05677385-7a7f-4545-8438-af00dde85db0
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6e1cc33d1a84f5f8a3cd186b148f57e296a350f4
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugprocess2enumthreads"></a>IDebugProcess2::EnumThreads
Pobiera listę wszystkie wątki uruchomione w procesie.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT EnumThreads(  
   IEnumDebugThreads2** ppEnum  
);  
```  
  
```csharp  
int EnumThreads(  
   out IEnumDebugThreads2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnum`  
 [out] Zwraca [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md) obiekt, który zawiera listę wszystkich wątków w wszystkie programy w procesie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda wylicza wątki uruchomione w każdym program i łączy je do widoku wątków procesu. Pojedynczy wątek może działać w wielu programach; Ta metoda wylicza wątek tylko raz.  
  
 Ta metoda Wyświetla listę wątków procesu bez duplikaty. W przeciwnym razie wyliczyć wątki uruchomione w szczególności program, użyj [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [EnumThreads](../../../extensibility/debugger/reference/idebugprogram2-enumthreads.md)