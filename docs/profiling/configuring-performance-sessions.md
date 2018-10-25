---
title: Konfigurowanie sesji wydajności | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- common tasks, performance
- common tasks, profiling tools
- profiling tools, common tasks
- performance, gathering data
ms.assetid: e1c3ba41-ffca-4edf-9a7f-8a5a9244ef9b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1e00c31643a5f894612daa24d4a271856d8e21f1
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49853444"
---
# <a name="configure-performance-sessions"></a>Konfigurowanie sesji wydajności
Za pomocą [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profiling Tools można zbierać szeroką gamę danych wydajności dla wielu typów aplikacji. W tej sekcji dowiesz się, jak za pomocą właściwości Wizardand wydajność sesji wydajności i docelowy plik binarny Konfigurowanie narzędzi profilowania do zbierania danych, który Cię interesuje. Właściwości konfiguracji narzędzia profilowania można również do kontrolowania ilości danych zbieranych podczas uruchomienia profilowania. Aby uzyskać więcej informacji, zobacz [kontrolować zbieranie danych](../profiling/controlling-data-collection.md).  
  
> [!NOTE]
>  W wielu przypadkach przy użyciu właściwości domyślne kreatora wydajności jest skutecznym sposobem zbierania danych profilowania. Aby uzyskać więcej informacji, zobacz [początkujących przewodnik dotyczący profilowanie wydajności](../profiling/beginners-guide-to-performance-profiling.md) i [wprowadzenie](../profiling/getting-started-with-performance-tools.md).  
  
## <a name="common-tasks"></a>Wspólne zadania
  
| Zadanie | Powiązana zawartość |
| - | - |
| **Ustawianie podstawowych opcji profilowania:** należy skonfigurować [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] do korzystania z serwera symboli firmy Microsoft. Będzie to upewnij się, że masz dostęp do symboli, takich jak nazwy funkcji i parametrów, aby uzyskać bieżącą wersję Windows i innych aplikacji firmy Microsoft. Można również określić inne opcje ogólne, przed uruchomieniem sesji profilowania, takich jak system uprawnień do narzędzi profilowania i nazwy pliku danych profilowania. | -   [Porady: odwołanie do Windows informacje o symbolach](../profiling/how-to-reference-windows-symbol-information.md)<br />-   [Instrukcje: serializacja informacji o symbolach](../profiling/how-to-serialize-symbol-information.md)<br />-   [Porady: Ustawianie bieżącej sesji](../profiling/how-to-set-the-current-session.md)<br />-   [Porady: Ustawianie uprawnień](../profiling/how-to-set-permissions.md)<br />-   [Porady: Ustawianie opcji nazwy pliku danych wydajności](../profiling/how-to-set-performance-data-file-name-options.md) |
| **Określ dane, które mają być zbierane:** procedur, które służą do konfigurowania sesji profilowania są zależne od typ aplikacji docelowej, który chcesz przeprowadzić profilowanie i typ danych wydajności, które mają być zbierane. | -   [Porady: Wybieranie metod kolekcji](../profiling/how-to-choose-collection-methods.md)<br />-   [Zbieranie statystyk wydajności za pomocą próbkowania](../profiling/collecting-performance-statistics-by-using-sampling.md)<br />-   [Zbieranie danych alokacji i okresie istnienia pamięci platformy .NET](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [Zbieranie szczegółowych danych o chronometrażu przy użyciu Instrumentacji](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)<br />-   [Porady: profilowanie kodu JavaScript na stronach sieci web](../profiling/how-to-profile-javascript-code-in-web-pages.md)<br />-   [Zbieranie danych współbieżności procesu i wątku](../profiling/collecting-thread-and-process-concurrency-data.md)<br />-   [Zbieranie dodatkowych danych o wydajności](../profiling/collecting-additional-performance-data.md) |
| **Ustawianie opcji konfiguracji zaawansowanej:** podczas profilowania aplikacji .NET Framework, które załadować wiele wersji wspólnego języka środowiska wykonawczego języka wspólnego (CLR) można określić, którą wersję profilu. Jeśli masz wiele plików .exe w sesji wydajności, można ustawić kolejność rozruchu plików binarnych. | -   [Porady: Określanie środowiska uruchomieniowego .NET Framework](../profiling/how-to-specify-the-dotnet-framework-runtime.md)<br />-   [Porady: Określanie plików binarnych do uruchomienia](../profiling/how-to-specify-the-binary-to-start.md) |
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Sterowanie zbieraniem danych](../profiling/controlling-data-collection.md)  
  
## <a name="see-also"></a>Zobacz także  
 [Eksplorator wydajności](../profiling/performance-explorer.md)