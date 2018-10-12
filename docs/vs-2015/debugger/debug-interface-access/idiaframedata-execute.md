---
title: Idiaframedata::EXECUTE — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::execute method
ms.assetid: 7a6c7d03-1ff1-4059-bd54-5f407eeebc26
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f8949e0a9c0f7aac0a648df9de8ee50c4f32292c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49197772"
---
# <a name="idiaframedataexecute"></a>IDiaFrameData::execute
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Wykonuje odwijanie stosu i zwraca wyniki w interfejsie ramki przeszukiwania stosu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT execute (   
   IDiaStackWalkFrame* frame  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `frame`  
 [in] [Idiastackwalkframe —](../../debugger/debug-interface-access/idiastackwalkframe.md) obiekt, który zawiera stan rejestrów ramki.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. W poniższej tabeli przedstawiono możliwe wartości zwracane dla tej metody.  
  
|Wartość|Opis|  
|-----------|-----------------|  
|E_DIA_INPROLOG|Nie można wykonać ramkę stosu w kodzie prologu.|  
|E_DIA_SYNTAX|Błąd wystąpił w programie ramki analizy.|  
|E_DIA_FRAME_ACCESS|Nie można rejestrów dostępu lub pamięci.|  
|E_DIA_VALUE|Wystąpił błąd podczas obliczania wartości (na przykład, dzielenie przez zero).|  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest wywoływana podczas debugowania do odkręcanie stosu. [Idiastackwalkframe —](../../debugger/debug-interface-access/idiastackwalkframe.md) obiektu jest implementowany przez aplikację klienta, aby otrzymywać aktualizacje w rejestrach i dostarcza metod używanych przez `execute` metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaframedata —](../../debugger/debug-interface-access/idiaframedata.md)   
 [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md)



