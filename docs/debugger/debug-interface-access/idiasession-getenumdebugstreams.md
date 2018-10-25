---
title: Idiasession::getenumdebugstreams — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::getEnumDebugStreams method
ms.assetid: d294954b-80e9-476c-b9f0-5ca6fd575f68
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 53eb0765b7a3d9ed5fb23c0b1d8880eeca390159
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49818800"
---
# <a name="idiasessiongetenumdebugstreams"></a>IDiaSession::getEnumDebugStreams
Pobiera sekwencję wyliczany strumieni danych debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT getEnumDebugStreams (   
   IDiaEnumDebugStreams** ppEnumDebugStreams  
)  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnumDebugStreams`  
 [out] Zwraca [idiaenumdebugstreams —](../../debugger/debug-interface-access/idiaenumdebugstreams.md) obiektu, który zawiera listę strumienie debugowania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaEnumDebugStreams](../../debugger/debug-interface-access/idiaenumdebugstreams.md)