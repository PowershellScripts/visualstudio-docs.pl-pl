---
title: CPU i liczniki Windows | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.counters
helpviewer_keywords:
- Windows counters in Profiling Tools
- CPU counters in Profiling Tools
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 585fb2fa8d2662d1a2bec7915bf1f08a4dc771e4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49865924"
---
# <a name="cpu-and-windows-counters"></a>Liczniki procesora CPU i systemu Windows

Visual Studio Profiler umożliwia zbieranie danych wydajności, który został wygenerowany przez system operacyjny (liczniki Windows) i dane wydajności, który został wygenerowany przez jednostkę procesora (liczniki CPU).

> [!NOTE]
> Ulepszone funkcje zabezpieczeń w systemie Windows 8 i Windows Server 2012 wymagają znaczących zmian w taki sposób, programu Visual Studio profiler zbiera dane na tych platformach. Aplikacje platformy uniwersalnej systemu Windows również wymagają nowych technik zbierania. Zobacz [narzędzia do oceny wydajności w aplikacjach systemu Windows 8 i Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="windows-counters"></a>Liczniki Windows

Windows liczniki są częścią infrastruktury diagnostycznej Windows, który zawiera informacje o wydajności systemu operacyjnego lub aplikacji, usługi lub sterownika. Liczniki Windows zależą od konfiguracji bieżącego komputera i mogą nie być dostępne na innych komputerach. Liczniki wydajności Windows są gromadzone w pliku danych jako znaczników, które następnie mogą być używane do filtrowania, widoki i raporty profilowania profilowania.

## <a name="cpu-counters"></a>Liczniki procesora CPU

Liczniki procesora CPU są funkcją procesora komputera, które przechowują liczbę zdarzeń związanych ze sprzętem. Podczas zbierania danych licznika Procesora przy użyciu Instrumentacji, metoda profilowania, dane są dołączane do danych dla funkcji i modułów. Możesz zbierać wiele liczników CPU przy użyciu metody instrumentacji. Korzystając z metody pobierania próbek, możesz wybrać jeden licznik do użycia jako zdarzenia mają być pobrane próbki.

Liczniki wydajności są specyficzne dla procesora CPU. Różne modele i wersje Procesora mogą mieć znacząco różnych ustawień konfiguracji umożliwiające tego samego licznika wydajności. [!INCLUDE[vs_dev11_long](../data-tools/includes/vs_dev11_long_md.md)] Zdarzenia przenośne Profiler rozdzielenie kilka typowych liczników wydajności z określonych procesorów i umożliwiają zbieranie i przykładowe zdarzenia ogólnych problemów z wydajnością.

Jeśli zechcesz policzyć określonego zdarzenia, gdy używasz programu profilującego, na przykład Chybienia pamięci podręcznej L2, tworzyć sesji pomiaru wydajności wokół tego nadawcy zdarzeń. Można to zrobić na dowolny procesor CPU z pamięci podręcznej L2. Sesja wydajności można przenosić z platformami bez żadnych modyfikacji.

Profilera Visual Studio w dalszym ciągu obsługuje określonych zdarzeń dla określonej platformy. Na przykład Deweloper na platformie Pentium 4 chcieć liczba zdarzeń, które są specyficzne dla architektury NetBurst. To zdarzenie nie jest przenośny, ale nadal dostępne dla dewelopera dla sesji wydajności określonych na danej platformie.

## <a name="portable-and-platform-events"></a>Zdarzenia przenośne i platformy

Zdarzenia przenośne są grupy liczniki procesora CPU, które nie są specyficzne dla określonego procesora. Wszystkie liczniki procesora CPU są nazywane zdarzeń platformy i może nie być obsługiwany na różnych platformach.

 Liczniki dla zdarzenia przenośne i platformy są definiowane w. *xml* plików, w którym znajdują się określonej wartości, które są związane z licznikami. Istnieją różne procesory, wiele plików, ponieważ dane dotyczące firmy Intel i procesory AMD, na przykład różnią się. [!INCLUDE[vs_orcas_long](../debugger/includes/vs_orcas_long_md.md)] Profiler używa tych informacji do przedstawienia odpowiednich liczników, przenośne i platformy, dla użytkownika na potrzeby pomiaru wydajności.

### <a name="portable-events"></a>Zdarzenia przenośne

Zdarzenia przenośne zawierają następujące zdarzenia:

**Zdarzenia ogólne**

|Nazwa zdarzenia|Opis zdarzenia|
|----------------|-----------------------|
|Wycofane instrukcje|Wskazuje liczbę instrukcji, które wykonywane do momentu zakończenia zdarzenia.|
|Cykle niezatrzymane|Wskazuje tylko te cykle, w których procesor nie jest wyłączana, na przykład oczekiwania na We/Wy.|

**Zdarzenia frontonu**

|Nazwa zdarzenia|Opis zdarzenia|
|----------------|-----------------------|
|Chybienia buforu ITLB|Wskazuje liczbę wyszukiwania buforu wygląd odkładania do tłumaczenia instrukcji, które spowodowało trafienia.|

**Zdarzenia dotyczące gałęzi**

|Nazwa zdarzenia|Opis zdarzenia|
|----------------|-----------------------|
|Wycofane gałęzie|Wskazuje liczbę instrukcji gałęzi wykonywana do czasu zakończenia zdarzenia.|
|Źle przewidziane gałęzie|Wskazuje źle przewidziane gałęzie, które występują, ponieważ procesor przewidzieć ścieżka jest niepoprawna. Źle przewidziane gałęzie wpłynąć na wydajność, ponieważ procesor Odrzuć wszystkie prace wykonane i uruchom ponownie na poprawną ścieżkę.|

**Zdarzeń pamięci:**

|Nazwa zdarzenia|Opis zdarzenia|
|----------------|-----------------------|
|L2 Chybienia odczytu pamięci podręcznej|Wskazuje, że liczba drugiego poziomu pamięci podręcznej odczytu Chybienia.|
|L2 Odwołania odczytu pamięci podręcznej|Wskazuje, że liczba drugiego poziomu pamięci podręcznej odczytu odwołania. Zawiera Chybienia ładowania i przeczytaj Chybienia własności (RFO) i trafień.|

## <a name="view-available-counters"></a>Wyświetl dostępne liczniki

Możesz wyświetlić listę dostępne liczniki procesora CPU w środowisku IDE programu Visual Studio w oknie wiersza polecenia.

### <a name="visual-studio-ui"></a>Visual Studio UI

Aby wyświetlić listę dostępnych liczników na komputerze w środowisku IDE programu Visual Studio, konieczne jest posiadanie sesję wydajności programu profilującego, Otwórz w Eksploratorze wydajności.

#### <a name="to-view-a-list-of-a-list-of-all-cpu-counters-that-are-supported-on-the-current-platform"></a>Aby wyświetlić listę listę wszystkie liczniki procesora CPU, które są obsługiwane na bieżącej platformie

1. W Eksploratorze wydajności, kliknij prawym przyciskiem myszy sesję wydajności, a następnie kliknij przycisk **właściwości**.

2. Wykonaj jedną z następujących czynności:

   - Kliknij przycisk **próbkowania**, a następnie wybierz pozycję **licznika wydajności** z **przykładowe** listy zdarzeń. Liczniki procesora CPU są wymienione w **dostępnych liczników wydajności**.

      **Uwaga** kliknij **anulować** aby powrócić do poprzedniej konfiguracji pobierania próbek.

     —lub—

   - Wybierz **liczniki CPU**, a następnie wybierz pozycję **zbierania liczników Procesora**. Liczniki procesora CPU są wymienione w **dostępne liczniki**.

      **Uwaga** kliknij **anulować** aby powrócić do poprzedniej konfiguracji licznika w kolekcji.

#### <a name="to-view-a-list-of-a-list-of-window-counters-that-are-supported-on-the-current-platform"></a>Aby wyświetlić listę listę liczników okna, które są obsługiwane na bieżącej platformie

1. W Eksploratorze wydajności, kliknij prawym przyciskiem myszy sesję wydajności, a następnie kliknij przycisk **właściwości**.

2. Kliknij przycisk **liczniki Windows**.

3. Wybierz **Zbierz liczniki Windows**.

4. Z **kategorii licznika** , wybierz grupę liczników na liście. Licznik Windows grupy jest wyświetlana w polu listy.

     **Uwaga:** kliknij **anulować** aby powrócić do poprzedniej konfiguracji licznika w kolekcji.

### <a name="command-line"></a>Wiersz polecenia

Za pomocą [VSPerfCmd](../profiling/vsperfcmd.md) narzędzia wiersza polecenia, możesz wyświetlić listę liczniki procesora CPU, które są dostępne na komputerze z poziomu wiersza polecenia.

#### <a name="to-list-of-cpu-counters-that-are-supported-on-the-current-platform"></a>Na liście liczników procesora CPU, które są obsługiwane na bieżącej platformie

1. Otwórz okno wiersza polecenia.

2. Typ

     **\<Katalog narzędzi wydajności w usłudze Visual Studio >/querycounters \VSPerfCmd**

     gdzie  *\<katalogu narzędzi wydajności w usłudze Visual Studio >* zazwyczaj jest to ścieżka do narzędzia do oceny wydajności katalogu instalacji programu Visual Studio

     *C:\Program Files\Microsoft Visual Studio 10.0\Team narzędzia Tools*

## <a name="see-also"></a>Zobacz także

[Omówienia](../profiling/overviews-performance-tools.md)  
[Instrukcje: wybieranie zdarzeń próbkowania](../profiling/how-to-choose-sampling-events.md)  
[Instrukcje: zbieranie danych licznika procesora CPU](../profiling/how-to-collect-cpu-counter-data.md)  
[Porady: zbieranie danych licznika Windows](../profiling/how-to-collect-windows-counter-data.md)