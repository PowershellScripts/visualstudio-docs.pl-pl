---
title: Mierzenie wydajności kodu w języku Python
description: Jak używać programu Visual Studio profiler do sprawdzenia wydajności Python kodu podczas usnig interpretery na podstawie języka CPython.
ms.date: 11/12/2018
ms.prod: visual-studio-dev15
ms.technology: vs-python
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: douge
ms.workload:
- python
- data-science
ms.openlocfilehash: 0b5ca29b061f0ba61eec775a0344fb8d2067e08d
ms.sourcegitcommit: 6a955a2d179cd0e137942389f940d9fcbbe125de
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/13/2018
ms.locfileid: "51607487"
---
# <a name="profile-python-code"></a>Profiluj kod języka Python

Można profilować aplikacji w języku Python, używając interpretery na podstawie języka CPython. (Zobacz [tabela funkcji - profilowania](overview-of-python-tools-for-visual-studio.md#matrix-profiling) dostępność tej funkcji dla różnych wersji programu Visual Studio.)

## <a name="profiling-for-cpython-based-interpreters"></a>Profilowania na podstawie języka CPython interpretery

Profilowanie została uruchomiona przy użyciu **analizy** > **Uruchom profilowanie Python** polecenia menu, co spowoduje otwarcie okna dialogowego konfiguracji:

![Okno dialogowe konfiguracji profilowania](media/profiling-start.png)

Po wybraniu **OK**, program profilujący jest uruchamiany i otwiera raport wydajności za pomocą którego możesz eksplorować, jak czas w aplikacji:

![Raport profilowania wydajności](media/profiling-results.png)

|   |   |
|---|---|
| ![Ikona aparatu film wideo](../install/media/video-icon.png "Obejrzyj klip wideo") | [Obejrzyj film wideo (Microsoft Virtual Academy)](https://mva.microsoft.com/en-US/training-courses-embed/python-tools-for-visual-studio-2017-18121/Video-Profiling-Python-s6FoC6LWE_1005918567) demonstracyjne Python profilowania (3 m 00s).|

> [!Note]
> Obecnie program Visual Studio obsługuje tylko na tym poziomie profilowania pełnej aplikacji, ale chcemy poznać Twoją opinię na temat przyszłych funkcji bez obaw. Użyj [ **opinie o produkcie** przycisk](#feedback) u dołu tej strony.

## <a name="profiling-for-ironpython"></a>Profilowanie w przypadku v Ironpythonu

Ponieważ IronPython interpreterem na podstawie języka CPython, powyżej funkcji profilowania nie działa.

Zamiast tego należy użyć profilera Visual Studio .NET, uruchamiając *ipy.exe* bezpośrednio w aplikacji docelowej za pomocą odpowiednie argumenty do uruchomienia skryptu uruchamiania. Obejmują `-X:Debug` w wierszu polecenia, aby upewnij się, że wszystkie Twoje Python kod może być debugowania i profilowania. Ten argument wygenerowanie raportu dotyczącego wydajności, w tym czas środowiska uruchomieniowego IronPython i kodu. Twój kod jest identyfikowany przy użyciu zniekształcone nazwy.

Alternatywnie IronPython ma kilka swój własny profilowanie wbudowana, ale nie ma obecnie nie dobrej Wizualizator dla niego. Zobacz [Profiler IronPython](https://blogs.msdn.microsoft.com/curth/2009/03/30/an-ironpython-profiler/) (blogi MSDN) na co jest dostępne.
