---
title: Czas synchronizacji | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.synchronization
helpviewer_keywords:
- Concurrency Visualizer, Synchronization Time
ms.assetid: affa04cc-8bba-4848-9301-b19846d3c2cb
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 67f63f292a20e21a00f733dd1190521fd573b98b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49861179"
---
# <a name="synchronization-time"></a>Czas synchronizacji
Te segmenty na osi czasu są skojarzone z zablokowania prób są klasyfikowane jako synchronizacji. Gdy wątek jest oznaczony jako zablokowane na synchronizacji, jeden z nich jest implikowane:  
  
- Wykonywanie wątku może spowodować utworzenie wywołanie synchronizacji wątków dobrze znanych interfejsów API takich jak `EnterCriticalSection()` lub `WaitForSingleObject()`.  
  
- Algorytm dopasowania interfejsu API nie może być całkowicie kompleksowe i w związku z tym niektóre interfejsy API, który mógłby być mapowany na innych kategoriach może również wystąpić, ponieważ synchronizacji, ponieważ ramki w wywołaniu stosu po pewnym czasie osiągnięto bazowego jądra blokuje pierwotnych, która została mapowany do tej kategorii.  
  
  Aby zrozumieć przyczyny wydarzeniu blokowania wątku, należy dokładnie bada blokowania stosy wywołań i profilu, raportów.  
  
## <a name="see-also"></a>Zobacz także  
 [Widok wątków](../profiling/threads-view-parallel-performance.md)