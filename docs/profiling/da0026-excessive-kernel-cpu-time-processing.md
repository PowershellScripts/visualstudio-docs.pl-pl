---
title: 'DA0026: Nadmierne CPU jądra. czas przetwarzania | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DA0026
- vs.performance.DA0026
- vs.performance.26
ms.assetid: 4cfc8a29-b29b-4a72-b386-03d8856fdf8a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9043b1dddcacc797c640252691d6bf393189cc4d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49876610"
---
# <a name="da0026-excessive-kernel-cpu-time-processing"></a>DA0026: Nadmierne przetwarzanie czasu procesora CPU w trybie jądra

|||  
|-|-|  
|Identyfikator reguły|TODO|  
|Kategoria|Użycie narzędzia profilowania|  
|Metoda profilowania|Próbkowania|  
|Komunikat|Został zmierzony stosunkowo dużej ilości czasu Procesora w trybie jądra. Należy rozważyć zbadanie kodu źródłowego z włączonym próbkowaniem SysCall.|  
|Typ reguły|Informacje|  

 Podczas profilowania za pomocą próbkowania pamięci platformy .NET i metod rywalizacji zasobów musi zebrać co najmniej 10 próbek do wyzwolenia tej reguły.  

## <a name="cause"></a>Przyczyna  
 Czas procesora CPU udział, który został wykonany w trybie jądra przekracza ilość czasu spędzonego w trybie użytkownika. Należy wziąć pod uwagę profilowanie ponownie i próbkowanie liczba wywołań systemowych (syscalls) w celu ustalenia przyczyny od czasu wykonania trybu jądra wysoka.  

## <a name="rule-description"></a>Opis reguły  
 Stosunkowo dużą część czas potrzebny aplikacji do wykonywania w trybie jądra mogą uzasadniać dalszego badania. Aplikacja w trybie użytkownika przechodzi do trybu jądra do wykonywania operacji We/Wy, poczekaj, aż wątek lub procesu synchronizacji w nim elementów podstawowych lub wykonać wywołania systemowe. Można zbadać rodzaje wywołań systemowych sprawia, że aplikacja, i funkcje, które odpowiadają po wybraniu opcji, aby zebrać stosy wywołań przykładowe opartym na wywołania systemowe.  

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby zbadać rodzaje wywołań systemowych, wykonywanych przez aplikację, ponownie uruchom profil i wybierz opcję, aby zebrać przykładów, w oparciu o wywołania systemowe. Zobacz [porady: Wybieranie zdarzeń próbkowania](../profiling/how-to-choose-sampling-events.md) w przypadku korzystania z narzędzi profilowania w IDE, aby uzyskać więcej informacji. Jeśli używasz narzędzi profilowania z wiersza polecenia, zobacz **przykładowe opcje interwału** części [VSPerfCmd](../profiling/vsperfcmd.md) artykułu w odwołaniu do narzędzia wiersza polecenia Profiling Tools.