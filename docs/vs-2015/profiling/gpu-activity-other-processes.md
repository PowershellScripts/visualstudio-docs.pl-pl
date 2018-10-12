---
title: Aktywność procesora GPU (inne procesy) | Dokumentacja firmy Microsoft
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
- vs.cv.threads.timeline.gpuother
- vs.cv.threads.timeline.gpuactivity
ms.assetid: 8a68df65-eb63-452f-9285-fb4ffc92f2b2
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3d988ab3e381ef8c5d25eed1978eed39c53e9e24
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49272145"
---
# <a name="gpu-activity-other-processes"></a>Aktywność procesora GPU (inne procesy)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Aktywność procesora GPU (inne procesy)** segmenty w widoku wątków narzędzia Concurrency visualizer reprezentują czas, kiedy procesora GPU przetwarzającą żądania w imieniu innych procesów w systemie. Te żądania są wysyłane przez GPU jako pakiety dostępu (DMA) pamięci.  Długość segmentu reprezentuje czas przetwarzania pakietu przez GPU.  
  
 Po wybraniu tego rodzaju segmentu, raport na **bieżącego** karta zawiera informacje o pakiecie, która została przetworzona.  Informacje obejmują czas, który pakiet jest oczekiwany w kolejce sprzętowej, skojarzony z aparatu programu DirectX, proces, który przesłał pakiet i czas wymagany do przetwarzania pakietów.



