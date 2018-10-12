---
title: Widok podsumowania — widok Kontencji zasobów | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Summary view
ms.assetid: 6da57b83-7b42-4d7c-9aea-8e0a830faf6b
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7cf00fbb7237194b88edc9e748abfa06483a44a5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49229752"
---
# <a name="summary-view---resource-contention-view"></a>Widok podsumowania — widok rywalizacji o zasoby
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Widok podsumowania Wyświetla informacje o zdarzeniach w Twojej aplikacji, w którym wątku lub procesu zostało wstrzymane, podczas gdy oczekiwano dostęp do zasobu.  
  
 Aby uzyskać więcej informacji, łącznie z opisem powiadomienie łącza i listy raportów, zobacz [Widok Podsumowanie](../profiling/summary-view.md).  
  
## <a name="timeline-graph"></a>Wykres osi czasu  
 Wykres osi czasu w widoku podsumowania przedstawia liczbę zdarzeń rywalizacji o zasoby w profilowanej aplikacji wraz z upływem czasu, który wystąpił profilowania. Wykres osi czasu można użyć do filtrowania widoku, aby w wybranym okresie. Aby uzyskać więcej informacji, zobacz [jak: Filtr widoków raportu z podsumowania osi czasu](../profiling/how-to-filter-report-views-from-the-summary-timeline.md).  
  
## <a name="most-contended-resources"></a>Zasoby z największą rywalizacją  
 **Większość zasobów z rywalizacją** zawiera listę zasobów w aplikacji, która spowodowała najbardziej zdarzenia rywalizacji. Kliknięcie nazwy zasobu, aby wyświetlić widok rywalizacji. Widok Kontencji zapewnia szczegółowe oś czasu rywalizacji zasobów przez wątek.  
  
 **Większość zasobów z rywalizacją** zawiera następujące dane dla każdego zasobu.  
  
|Kolumny|Opis|  
|------------|-----------------|  
|**Nazwa**|Nazwa zasobu.|  
|**% Rywalizacji**|Procent wszystkich zdarzeń rywalizacji o zasoby w danych profilowania, które były rywalizacji za pośrednictwem tego zasobu.|  
  
## <a name="most-contended-thread"></a>Najbardziej rywalizacją wątku  
 **Większość wątków z rywalizacją** Wyświetla listę wątków w aplikacji, która ma największą liczbę zdarzeń rywalizacji o zasoby. Kliknięcie nazwy wątku, aby wyświetlić widok rywalizacji, który dostarcza szczegółowe oś czasu rywalizacji zasobów przez wątek.  
  
 **Większość wątków z rywalizacją** zawiera następujące dane dla każdego wątku.  
  
|Kolumny|Opis|  
|------------|-----------------|  
|**ID**|Identyfikator wątku.|  
|**Nazwa**|Nazwa procesu, który jest właścicielem wątku.|  
|**% Rywalizacji**|Procent wszystkich zdarzeń rywalizacji o zasoby w danych profilowania, które były rywalizacji za pośrednictwem tego zasobu.|



