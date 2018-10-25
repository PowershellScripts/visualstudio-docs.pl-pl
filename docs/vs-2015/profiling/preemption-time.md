---
title: Czas wywłaszczania | Dokumentacja firmy Microsoft
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
- vs.cv.threads.timeline.preemption
helpviewer_keywords:
- Concurrency Visualizer, Preemption Time
ms.assetid: 6b78f91e-a006-440c-83fb-e7368040951d
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f302dff3ea72217c6325aca667aec8ff4d7f218f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49905236"
---
# <a name="preemption-time"></a>Czas wywłaszczania
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Te segmenty na osi czasu są skojarzone z czasu blokowania, które należą do kategorii Wywłaszczania. Ta kategoria wynika, że wątek jest przełączenie ze względu na jeden z następujących powodów:  
  
- Harmonogram zastąpiono ją za pomocą wyższy priorytet wątku.  
  
- Wygasłe quantum wykonanie wątku, i inne wątki były gotowe do wykonania.  
  
  W tym czasie wątek został zablokowany przez jądro powód oczekiwania, który zlicza Concurrency Visualizer jako Wywłaszczania. Wywłaszczanie segmentów Uruchom gdy wątek jest przekazywane poza rdzeń logiczny, a kończyć, kiedy wątek wznawia działanie.  
  
  Etykietka narzędzia dla segmentu preempted Wyświetla nazwę proces lub wątek, który spowodował wywłaszczania. Jednak to nie oznacza, że proces lub wątek, który zajął stanowisko dyrektora faktycznie uruchomiła przez cały okres preempted.  
  
## <a name="see-also"></a>Zobacz też  
 [Widok wątków](../profiling/threads-view-parallel-performance.md)



