---
title: "Reguły wydajności monitorowania zasobu | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: f0f77faf-0a05-4718-a2c5-47934be40868
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: aed7363a51b08359fc5023cbbd9b7df1b7b7f8cd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="resource-monitoring-performance-rules"></a>Reguły wydajności monitorowania zasobu
Komunikaty wydajności w kategorii monitorowania zasobów zawierają dodatkowe dane dotyczące wydajności aplikacji. Można użyć tych danych do analizowania problemów z wydajnością. Te reguły są informacyjny i podać dla każdego przebiegu profilowania.  
  
|||  
|-|-|  
|[DA0501: Średnie wykorzystanie CPU przez proces poddawany profilowaniu.](../profiling/da0501-average-cpu-consumption-by-the-process-being-profiled.md)|Ten komunikat raporty procent czasu, który procesor był zajęty wykonywaniem instrukcji z aplikacji. Podanej wartości jest średnią we wszystkich interwałach pomiarowych, w których był aktywny PROFILOWANEGO procesu.|  
|[DA0502: Maksymalne wykorzystanie CPU przez proces poddawany profilowaniu](../profiling/da0502-maximum-cpu-consumption-by-the-process-being-profiled.md)|Ten komunikat raporty maksymalny procent czasu, przez który procesor był zajęty wykonywaniem instrukcji z aplikacji. Podanej wartości jest wartość maksymalna zgłoszone wśród wszystkich interwałów pomiarowych, w których był aktywny PROFILOWANEGO procesu.|  
|[DA0503: Średni rozmiar zestawu roboczego w bajtach dla procesu poddawanego profilowaniu](../profiling/da0503-average-working-set-in-bytes-for-the-process-being-profiled.md)|Ten komunikat raporty średnia ilość pamięci fizycznej w bajtach, przez proces używał podczas profilowania był aktywny. Tę miarę fizycznej pamięci jest określany jako zestaw roboczy.|  
|[DA0504: Maksymalny rozmiar zestawu roboczego w bajtach dla procesu poddawanego profilowaniu](../profiling/da0504-maximum-working-set-in-bytes-for-the-process-being-profiled.md)|Ten komunikat raporty maksymalną ilość pamięci fizycznej w bajtach, przez proces używał podczas profilowania był aktywny.|  
|[DA0505: Średnie Bajty prywatne przydzielone dla procesu poddawanego profilowaniu](../profiling/da0505-average-private-bytes-allocated-for-the-process-being-profiled.md)|Ten komunikat raporty średnia ilość pamięci wirtualnej, że proces przydzielone w bajtach podczas profilowania był aktywny. Tę miarę pamięci wirtualnej jest nazywany *bajtów prywatnych*. Bajty prywatne reprezentuje lokalizacje pamięci wirtualnej, które zostały przydzielonej przez proces, który jest dostępny tylko przez wątki uruchomione wewnątrz procesu.|  
|[DA0506: Maksymalne Bajty prywatne przydzielone dla procesu poddawanego profilowaniu](../profiling/da0506-maximum-private-bytes-allocated-for-the-process-being-profiled.md)|Ten komunikat raporty maksymalną ilość pamięci wirtualnej, że proces przydzielone w bajtów prywatnych podczas profilowania był aktywny.|