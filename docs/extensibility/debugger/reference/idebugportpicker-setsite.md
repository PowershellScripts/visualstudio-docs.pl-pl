---
title: IDebugPortPicker::SetSite | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- IDebugPortPicker::SetSite
ms.assetid: 7319e187-adfe-4b3f-aec9-521356fb5a8a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 00730a5338a3355f2397a91bc7a3693b30dca31b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49930612"
---
# <a name="idebugportpickersetsite"></a>IDebugPortPicker::SetSite
Ustawia dostawcę usług.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT SetSite(  
   IServiceProvider * pSP  
);  
```  
  
```csharp  
public int SetSite(  
   IServiceProvider pSP  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pSP`  
 [in] Odwołanie do interfejsu dostawcę usług.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda zostanie wywołana przed inne metody są wywoływane.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugPortPicker](../../../extensibility/debugger/reference/idebugportpicker.md)