---
title: IDebugDefaultPort2::GetServer | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugDefaultPort2::GetServer
helpviewer_keywords:
- IDebugDefaultPort2::GetServer
ms.assetid: cacb4b74-0f39-471c-af38-54b73f5b2868
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 273e6b89ce9ca38c05034ae1b31e4eeb9fec5b86
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49874374"
---
# <a name="idebugdefaultport2getserver"></a>IDebugDefaultPort2::GetServer
Ta metoda pobiera interfejs do serwera, na którym znajduje się na tym porcie.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetServer(  
   IDebugCoreServer3** ppServer  
);  
```  
  
```csharp  
int GetServer(  
   out IDebugCoreServer3 ppServer  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppServer`  
 [out] Zwraca obiekt Implementowanie [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md) interfejsu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md) jest implementowany przez program Visual Studio i reprezentuje serwer, który port znajduje się na.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)   
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)