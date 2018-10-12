---
title: Pusty Segment osi czasu | Dokumentacja firmy Microsoft
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
- vs.cv.threads.timeline.empty
helpviewer_keywords:
- Concurrency Visualizer, empty timeline segment
ms.assetid: f37b301f-3edc-4e56-8084-feec2dc5a9b1
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7f163b87365214a04a2643b7f256b72184fa69aa
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49256740"
---
# <a name="empty-timeline-segment"></a>Pusty segment osi czasu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W Wizualizatorze współbieżności, przyczyna, dla której części osi czasu jest pusty (ma białe tło) jest zależna od typu kanału.  
  
-   Dla kanału wątku procesora CPU oznacza to, że wątek nie istniał w tej części osi czasu. Jeśli interesuje Cię wątku, można znaleźć sekcji wykonywanie używający kontroli powiększenia lub przewijanie w poziomie.  
  
-   W przypadku kanałem we/wy oznacza to, nie dostępu do dysku wystąpił w danym momencie imieniu procesu docelowego.  
  
-   Dla kanału DirectX oznacza to, że nie działanie procesora GPU zostało wykonane imieniu procesu docelowego podczas tej części osi czasu.  
  
-   Kanału znacznika oznacza to, czy nie wygenerowano żadnych znaczników.  
  
## <a name="see-also"></a>Zobacz też  
 [Widok wątków](../profiling/threads-view-parallel-performance.md)   
 [Ustawianie powiększenia (Widok wątków)](../profiling/zoom-control-threads-view.md)



