---
title: IDiaStackWalker::getEnumFrames | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalker2::getEnumFrames method
ms.assetid: f9f09729-4c34-441c-989c-e0b7339ee32c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f4c7d8d30dee1d9c0a058177ad54aab864cee28d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49836166"
---
# <a name="idiastackwalkergetenumframes"></a>IDiaStackWalker::getEnumFrames
Pobiera moduł wyliczający ramek stosu dla x86 platform.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT getEnumFrames(   
   IDiaStackWalkHelper*   pHelper,  
   IDiaEnumStackFrames**  ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pHelper`  
 [in] Pomocnik [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md) obiektu.  
  
 `ppEnum`  
 [out] Zwraca [idiaenumstackframes —](../../debugger/debug-interface-access/idiaenumstackframes.md) obiekt, który zawiera listę [idiastackframe —](../../debugger/debug-interface-access/idiastackframe.md) obiektów.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Aby uzyskać listę ramek stosu na inne platformy, należy wywołać [IDiaStackWalker::getEnumFrames2](../../debugger/debug-interface-access/idiastackwalker-getenumframes2.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiastackwalker —](../../debugger/debug-interface-access/idiastackwalker.md)   
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [Idiastackframe —](../../debugger/debug-interface-access/idiastackframe.md)   
 [IDiaStackWalker::getEnumFrames2](../../debugger/debug-interface-access/idiastackwalker-getenumframes2.md)