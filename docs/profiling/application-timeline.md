---
title: "Analiza wykorzystania zasobów aplikacji XAML w programie Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: H1Hack27Feb2017
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: df7d854b-0a28-45a9-8a64-c015a4327701
caps.latest.revision: "11"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 32d6ac2581f71196d1f1d826d8f1024906b7cab9
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="analyze-resource-consumption-and-ui-thread-activity-xaml"></a>Analizowanie zużycia zasobów i aktywności wątku interfejsu użytkownika (XAML)
Użyj **oś czasu aplikacji** profilera, tak aby Znajdowanie i rozwiązywanie problemów aplikacji interakcji dotyczące problemów z wydajnością w aplikacji XAML. To narzędzie pomaga w zwiększeniu wydajności aplikacji XAML zapewniając szczegółowy widok wykorzystania zasobów aplikacji. Można analizować czasu poświęconego przez aplikację przygotowywanie ramki interfejsu użytkownika (układu i renderowania), sieci i dysku żądań obsługi, a w scenariuszach, takich jak rozmiar uruchamiania aplikacji, ładowania stron i systemu Windows.  
  
 **Oś czasu aplikacji** jest jednym z narzędzi można uruchomić z poziomu **Debug / profilera wydajności...**  polecenia.  
  
 To narzędzie zastępuje **czasu odpowiedzi interfejsu użytkownika XAML** narzędzia, która jest częścią zestawu narzędzi diagnostycznych dla programu Visual Studio 2013.  
  
 Za pomocą tego narzędzia, na następujących platformach:  
  
1.  Aplikacje uniwersalne systemu Windows (w systemie Windows 10)  
  
2.  Windows 8.1  
  
3.  Windows Phone 8.1 (wspólnej platformie XAML)  
  
4.  Program Windows Presentation Foundation (.Net 4.0 i nowsze)  
  
5.  Windows 7  
  
> [!NOTE]
>  Można zbierać i analizować dane użycia procesora CPU i dane dotyczące zużycia energii wraz z **ApplicationTimeline** danych. Zobacz [uruchamiania narzędzia profilowania z lub bez debuger](../profiling/running-profiling-tools-with-or-without-the-debugger.md).
  
##  <a name="BKMK_Collect_Timeline_data_for_your_app"></a>Zbieranie oś czasu aplikacji danych  
 Czas odpowiedzi aplikacji można profilu na komputerze lokalnym, podłączonego urządzenia, symulator Visual Studio lub emulatory lub urządzenie zdalne. Zobacz [uruchamiania narzędzia profilowania z lub bez debuger](../profiling/running-profiling-tools-with-or-without-the-debugger.md).
  
> [!TIP]
>  Jeśli to możliwe Uruchom aplikację bezpośrednio na urządzeniu. Wydajność aplikacji na symulatorze lub za pomocą połączenia pulpitu zdalnego może nie być taka sama jak rzeczywista wydajność na urządzeniu. Z drugiej strony zbieranie danych przy użyciu programu Visual Studio Tools zdalnego nie wpływa na dane wydajności.  
  
 Poniżej przedstawiono podstawowe kroki:  
  
1.  Otwórz aplikację języka XAML.  
  
2.  Kliknij przycisk **Debug / profilera wydajności...** . Należy wyświetlić listę narzędzia w oknie .diagsession profilowania.  
  
3.  Wybierz **oś czasu aplikacji** , a następnie kliknij przycisk **Start** w dolnej części okna.  
  
    > [!NOTE]
    >  Okno Kontrola konta użytkownika, Twoje uprawnienia do uruchamiania VsEtwCollector.exe żądanie może być widoczna. Kliknij przycisk **Tak**.  
  
4.  Uruchom scenariusz myślisz profilowania aplikacji w celu zbierania danych dotyczących wydajności.  
  
5.  Aby zatrzymać profilowanie, Przełącz do okna .diagsession, a następnie kliknij przycisk **zatrzymać** w górnej części okna.  
  
     Program Visual Studio analizuje zebrane dane i wyświetla wyniki.  
  
     ![Oś czasu profilera raport](../profiling/media/timeline_base.png "TIMELINE_Base")  
  
##  <a name="BKMK_Analyze_Timeline_profiling_data"></a>Analizowanie danych profilowania osi czasu  
 Po zebraniu danych profilowania można wykonać poniższe kroki, aby rozpocząć analizę:  
  
1.  Zapoznaj się z informacjami w **użycie wątków interfejsu użytkownika** i **przepływność wizualną (kl. / s)** wykresach, a następnie wybierz zakres czasu, które mają być analizowane za pomocą pasków nawigacji osi czasu.  
  
2.  Korzystając z informacji w **użycie wątków interfejsu użytkownika** lub **przepływność wizualną (kl. / s)** wykresy, sprawdź szczegóły w **szczegóły osi czasu** widok, aby wykryć możliwe przyczyny dla jawnego brak reakcji.  
  
###  <a name="BKMK_Report_scenarios_categories_and_events"></a>Scenariusze raportu, kategorie i zdarzenia  
 **Oś czasu aplikacji** narzędzie wyświetla dane chronometrażu dla scenariuszy, kategorii i zdarzenia, które są związane z wydajnością XAML.  
  
###  <a name="BKMK_Diagnostic_session_timeline"></a>Oś czasu sesji diagnostycznej  
 ![Wydajność i Diagnostyka osi czasu](../profiling/media/diaghub_timelinewithusermarks.png "DIAGHUB_TimelineWithUserMarks")  
  
 Linijki w górnej części strony przedstawiono oś czasu PROFILOWANEGO informacji. Oś czasu dotyczy zarówno **użycie wątków interfejsu użytkownika** wykres i **przepływność wizualną** wykresu. Można zawęzić zakres raportu, przeciągając paski nawigacyjne na osi czasu w celu zaznaczenia segmentu osi czasu.  
  
 Na osi czasu są także wyświetlane wstawione znaczniki użytkownika oraz zdarzenia cyklu życia aktywacji aplikacji.  
  
###  <a name="BKMK_UI_thread_utilization_graph"></a>Wykres wykorzystania wątku interfejsu użytkownika  
 ![Wykres wykorzystania CPU](../profiling/media/timeline_cpuutilization.png "TIMELINE_CpuUtilization")  
  
 **Użycie wątków interfejsu użytkownika (%)** wykresu jest wykres słupkowy wyświetlający względną ilość czasu w kategorii, aby podczas zakresu kolekcji.  
  
###  <a name="BKMK_Visual_throughput_FPS_graph"></a>Wykres przepływność wizualną (kl. / s)  
 ![Wykres przepływność wizualną](../profiling/media/timeline_visualthroughput.png "TIMELINE_VisualThroughput")  
  
 **Przepływność wizualną (kl. / s)** wykres liniowy pokazuje klatek na sekundę Zagregowanych w wątku interfejsu użytkownika i kompozycji dla aplikacji.  
  
###  <a name="BKMK_Timeline_details_"></a>Szczegóły osi czasu  
 Widok szczegółów jest, gdzie będzie wydatków większość czasu analizowanie raportu. Przedstawia on szczegółowy widok wykorzystania procesora CPU aplikacji skategoryzowany przez podsystem Framework interfejsu użytkownika lub składnik systemu, które zużyte Procesora.  
  
 Obsługiwane są następujące zdarzenia:  
  
|||  
|-|-|  
|**Analiza kodu**|Czas poświęcony na tworzenie obiektów i analizy plików XAML.<br /><br /> Rozszerzanie **Parsowanie** w węźle **szczegóły osi czasu** Wyświetla łańcuch zależności wszystkich plików XAML, które zostały przeanalizować wyniku zdarzeń głównego. Umożliwi to zidentyfikować tworzenie analizowania i obiekt niepotrzebnych plików w scenariuszach poufnych wydajności i zoptymalizowania je.|  
|**Układ**|W dużych aplikacji tysiące elementy mogą być wyświetlane na ekranie, w tym samym czasie. Może to spowodować niska szybkość klatek interfejsu użytkownika i czas odpowiedzi aplikacji odpowiednio niska. Zdarzenie układu dokładnie określa koszt układania każdego elementu (tj. czas spędzony w rozmieszczanie, miary ApplyTemplate, ArrangeOverride i ArrangeOverride) i tworzy visual drzewa, w których uczestniczyła w przebiegu układu. Można użyć tej wizualizacji, aby ustalić, który drzew logicznej musi oczyszczania lub do oceny innych mechanizmów opóźnienia, aby zoptymalizować z przebiegu układu.|  
|**Renderowanie**|Czas poświęcony na rysunku elementów XAML do ekranu.|  
|**I / 0**|Czas poświęcony na pobieranie danych z lokalnego dysku lub z zasobów sieciowych, które są dostępne za pośrednictwem [Microsoft Windows Internet (WinINet) interfejsu API](https://msdn.microsoft.com/en-us/library/windows/desktop/aa385331.aspx).|  
|**Kod aplikacji**|Czas poświęcony na wykonywanie kodu aplikacji (użytkownika), który nie jest powiązana z analizy ani układu.|  
|**Inne XAML**|Czas poświęcony na wykonywanie kodu środowiska uruchomieniowego języka XAML.|  
  
> [!TIP]
>  Wybierz **użycie procesora CPU** narzędzia wraz z **oś czasu aplikacji** narzędzia podczas uruchamiania profilowania do widoku aplikacji metod, które są wykonywane w wątku interfejsu użytkownika. Przenoszenie kodu aplikacji długotrwałe do wątku w tle może zwiększyć czas odpowiedzi interfejsu użytkownika.  
  
####  <a name="BKMK_Customizing_Timeline_details_"></a>Dostosowywanie szczegóły osi czasu  
 Użyj **szczegóły osi czasu** narzędzi do sortowania, filtrowania i podaj adnotacje o **szczegóły osi czasu** zapisy.  
  
|||  
|-|-|  
|**Sortuj według**|Sortuj według czasu rozpoczęcia lub długość zdarzenia.|  
|![Grupuj zdarzenia według ramki](../profiling/media/timeline_groupbyframes.png "TIMELINE_GroupByFrames")|Dodaje lub usuwa najwyższego poziomu **ramki** kategorii, który grupuje zdarzenia przez ramki.|  
|![Lista szczegółów osi czasu filtrów](../profiling/media/timeline_filter.png "TIMELINE_Filter")|Filtruje listę wybranych kategorii i długość zdarzenia.|  
|![Dostosuj oś czasu szczegółowe informacje o](../profiling/media/timeline_viewsettings.png "TIMELINE_ViewSettings")|Umożliwia określenie adnotacje do zdarzenia.|  
  
## <a name="see-also"></a>Zobacz też  
 [Blog zespołu WPF: Nowego interfejsu użytkownika narzędzia analizy wydajności aplikacji WPF](http://blogs.msdn.com/b/wpf/archive/2015/01/16/new-ui-performance-analysis-tool-for-wpf-applications.aspx)  
 [Najlepsze praktyki wydajności dla aplikacji platformy uniwersalnej systemu Windows przy użyciu języka C++, C# i Visual Basic](http://msdn.microsoft.com/en-us/567bcefa-5da5-4e42-a4b8-1358c71adfa2)   
 [Optymalizacja wydajności aplikacji WPF](/dotnet/framework/wpf/advanced/optimizing-wpf-application-performance)  
 [Profilowanie w programie Visual Studio](../profiling/index.md)  
 [Przegląd funkcji profilowania](../profiling/profiling-feature-tour.md)