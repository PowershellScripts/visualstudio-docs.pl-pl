---
title: Czas zarządzania pamięcią | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.cv.threads.timeline.paging
helpviewer_keywords:
- Concurrency Visualizer, Paging Time
ms.assetid: 67af3509-3a7d-435d-bc37-5262448da915
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 391f231a604af3fe0c47242acf7ea49c67f40f34
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49181327"
---
# <a name="memory-management-time"></a>Czas zarządzania pamięcią
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Te segmenty na osi czasu są skojarzone z zablokowania prób są podzielone na zarządzanie pamięcią. Oznacza to, że wątek jest zablokowany przez zdarzenie, który jest skojarzony z operacji zarządzania pamięcią, takich jak stronicowania. W tym czasie wątek został zablokowany w stanie interfejsu API lub jądra Concurrency Visualizer jest liczy się jako zarządzania pamięcią. Obejmują one zdarzenia, takie jak Alokacja pamięci i stronicowania.  
  
 Sprawdź stosy wywołań skojarzone i profilu, aby lepiej zrozumieć podstawowe przyczyny bloki, które są podzielone na zarządzanie pamięcią raportów.  
  
## <a name="see-also"></a>Zobacz też  
 [Widok wątków](../profiling/threads-view-parallel-performance.md)



