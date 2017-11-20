---
title: IDiaEnumSegments::Item | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumSegments::Item method
ms.assetid: ee44dd55-39a0-4b7b-97ff-2e1226eeb2bd
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4d64a0af3523882278763551b5bc55efa2116586
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumsegmentsitem"></a>IDiaEnumSegments::Item
Pobiera segment za pomocą indeksu.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT Item (   
   DWORD         index,  
   IDiaSegment** segment  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 indeks  
 [in] Indeks o [idiasegment —](../../debugger/debug-interface-access/idiasegment.md) obiektu do pobrania. Indeks znajduje się w zakresie od 0 do `count`-1, gdy `count` zwróconego przez [IDiaEnumSegments::get_Count](../../debugger/debug-interface-access/idiaenumsegments-get-count.md) metody.  
  
 Segment  
 [out] Zwraca [idiasegment —](../../debugger/debug-interface-access/idiasegment.md) obiekt reprezentujący wybrane segmenty.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumsegments —](../../debugger/debug-interface-access/idiaenumsegments.md)   
 [Idiasegment —](../../debugger/debug-interface-access/idiasegment.md)