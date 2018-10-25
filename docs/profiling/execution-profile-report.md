---
title: Raport profilu wykonania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.execution
helpviewer_keywords:
- Concurrency Visualizer, Execution Profile Report
ms.assetid: c8128472-a8ed-46f4-b1c8-a25358d6f2c1
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: fa0800bcf6a4fedfbcd8c787b3cca89638e9bcb9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49935292"
---
# <a name="execution-profile-report"></a>Raport profilu wykonania
Raport profilu wykonania jest profil próbkowania tradycyjnych. Pobierane są mniej więcej co milisekund w okresach, gdy wątek jest uruchomiony na rdzeń logiczny, a Concurrency Visualizer tworzy drzewo wywołań typowe przy sortowania skumulowana zestaw przykładowych stosów. Może mieć wpływ na dane w tej tabeli, przez bieżącego zakresu czasu i ukrytych wątków i te filtry, które mogą być stosowane:  
  
- Jeśli wybrano opcję tylko mój kod, są wyświetlane tylko ramek stosu, które mają kod użytkownika i jeden poziom poniżej kod użytkownika.  
  
- Jeśli ustawiono wartość redukcji szumu, sortowane stosów, które mają mniej niż z określoną częstotliwością są odfiltrowywane z raportu  
  
  W poniższej tabeli przedstawiono kolumn w raporcie.  
  
|Kolumny|Opis|  
|------------|-----------------|  
|Nazwa|Nazwa funkcji dla poszczególnych poziomów stosu wywołań.|  
|Próbki włączne|Łączna liczba próbek, które są zbierane dla wszystkich stosów, agregowanych do tego poziomu drzewo stosu wywołań. Liczba (włącznie) jest sumą wyłącznych próbek dla tej funkcji i włącznie liczniki dla wszystkich jego węzłów podrzędnych.|  
|Próbki wyłączne|Całkowita liczba zebranych próbek, dla których ta funkcja jest najniższy poziom stosu wywołań.|  
|% Włącznie|Procent całkowitej liczby próbek, która jest wyświetlana w kolumnie włącznych próbek. Wartości procentowe są zaokrąglane do dwóch miejsc po przecinku.|  
|% Wyłącznego|Procent całkowitej liczby próbek, która jest wyświetlana w kolumnie wyłącznych próbek. Wartości procentowe są zaokrąglane do dwóch miejsc po przecinku.|  
|Szczegóły|W pełni kwalifikowana nazwa funkcji. Obejmuje to liczba wierszy, gdy będzie ona dostępna.|  
  
 W tej tabeli do raportu można zobaczyć w [czas wykonywania (Widok wątków)](../profiling/execution-time-threads-view.md) widoku.  
  
## <a name="see-also"></a>Zobacz także  
 [Widok wątków](../profiling/threads-view-parallel-performance.md)