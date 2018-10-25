---
title: IDebugErrorBreakpoint2::GetBreakpointResolution | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugErrorBreakpoint2::GetBreakpointResolution
helpviewer_keywords:
- IDebugErrorBreakpoint2::GetBreakpointResolution
ms.assetid: 1c2324ed-2a11-4e63-8f3a-f420c7a4018b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4ca913ec9110c22108b2e4125cc33a19336ad911
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49893770"
---
# <a name="idebugerrorbreakpoint2getbreakpointresolution"></a>IDebugErrorBreakpoint2::GetBreakpointResolution
Pobiera rozwiązanie błąd punktu przerwania, który opisuje błąd.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetBreakpointResolution(   
   IDebugErrorBreakpointResolution2** ppErrorResolution  
);  
```  
  
```csharp  
int GetBreakpointResolution(   
   out IDebugErrorBreakpointResolution2 ppErrorResolution  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppErrorResolution`  
 [out] Zwraca [IDebugErrorBreakpointResolution2](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2.md) obiektu, który opisuje błąd.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugErrorBreakpoint2](../../../extensibility/debugger/reference/idebugerrorbreakpoint2.md)   
 [IDebugErrorBreakpointResolution2](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2.md)