---
title: Wykres aktywności GPU | Dokumentacja firmy Microsoft
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
- vs.cv.cpu.graph.gpu
ms.assetid: d7c769af-95fb-49a3-b5ab-deafecee46fa
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 90e84dbe71b529aef3cfad20172f62d65f8871d9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230207"
---
# <a name="gpu-activity-graph"></a>Wykres aktywności GPU
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Wykres aktywności procesora GPU w Wizualizatorze współbieżności przedstawia poziomu aktywności DirectX w systemie, gdyż jest mierzone przez liczbę aparatów DirectX, które są używane wraz z upływem czasu.  Wykres nie pokazuje, które określonych aparatów były używane.  Aparat uznaje się będzie używana, jeśli przetwarza wszystkie działanie procesora GPU.  
  
## <a name="gpu-activity-graph-colors"></a>Kolory wykres aktywności procesora GPU  
 Zielony oznacza zużycia silników DirectX w bieżącym procesie.  
  
 Jasny zwykle wskazuje zużycia silników DirectX przez inne procesy w systemie. Aby zmniejszyć zużycia silników DirectX przez inne procesy, Zmniejsz liczbę innych procesów uruchomionych w systemie.  
  
 Oficjalny wskazuje dostępność nieużywane aparatów DirectX w systemie. Silników są dostępne dla procesu, jeśli możesz znaleźć dodatkowe możliwości w celu ich wykorzystania. Niektóre aparaty należy używać tylko dla określonych typów zadań.  
  
## <a name="see-also"></a>Zobacz też  
 [Widok wykorzystania](../profiling/utilization-view.md)



