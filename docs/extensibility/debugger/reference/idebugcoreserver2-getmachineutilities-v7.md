---
title: IDebugCoreServer2::GetMachineUtilities_V7 | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugCoreServer2::GetMachineUtilities_V7
helpviewer_keywords: IDebugCoreServer2::GetMachineUtilities_V7
ms.assetid: 64c1f08f-853b-4498-9810-29791581ef2f
caps.latest.revision: "17"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 301af8eb2e6b317a532fec6dfdd5ac64f62d12a9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugcoreserver2getmachineutilitiesv7"></a>IDebugCoreServer2::GetMachineUtilities_V7
Ta metoda pobiera narzędzia komputera dla serwera.  
  
> [!NOTE]
>  Ta metoda jest przestarzała: nie używaj ([!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] zawsze zwraca `E_NOTIMPL` Jeśli ta metoda jest wywoływana). Ze względów historycznych jest zachowane.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetMachineUtilities_V7(  
   IDebugMDMUtil2_V7** ppUtil  
);  
```  
  
```csharp  
int GetMachineUtilities_V7(  
   out IDebugMDMUtil2_V7 ppUtil  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppUtil`  
 [out] Zwraca `IDebugMDMUtil2_V7` interfejs, który reprezentuje informacje narzędzia maszyny.  
  
## <a name="return-value"></a>Wartość zwracana  
 Zawsze zwraca `E_NOTIMPL`, wskazujący, że metoda nie jest zaimplementowana.  
  
## <a name="remarks"></a>Uwagi  
 [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]zawsze zwraca `E_NOTIMPL` Jeśli ta metoda jest wywoływana.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)