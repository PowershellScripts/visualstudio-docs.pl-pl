---
title: 'Porady: Instrumentowanie autonomicznego składnika natywnego i zbieranie danych przy użyciu Profiler w wierszu polecenia o chronometrażu | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 36883074-9be8-4e90-a66f-7e87f21fcd30
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: d9a2d4e4b0a19464bfded0c49ed4262c8fa8877a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49884800"
---
# <a name="how-to-instrument-a-native-stand-alone-component-and-collect-timing-data-with-the-profiler-from-the-command-line"></a>Porady: Instrumentowanie autonomicznego składnika natywnego i zbieranie danych o chronometrażu przy użyciu profilera z wiersza polecenia
W tym temacie opisano sposób użycia [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] wiersza polecenia narzędzi Profilujących do Instrumentacji natywnych składnika, takiego jak C++. *plik exe* lub. *Biblioteka DLL* pliku oraz w celu zbierania danych o chronometrażu.  

> [!NOTE]
>  Narzędzia wiersza poleceń dla narzędzi profilowania znajdują się w *tools\performance Tools* podkatalog [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] katalogu instalacyjnego. Na komputerach 64-bitowym 64-bitowe i 32-bitowe wersje narzędzia są dostępne. Aby użyć narzędzi profilowania z wiersza polecenia, należy dodać ścieżkę narzędzi do zmiennej środowiskowej PATH okna wiersza polecenia lub dodać do niej samo polecenie. Aby uzyskać więcej informacji, zobacz [Określ ścieżkę do narzędzia wiersza polecenia](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  

 Aby zebrać szczegółowe dane czasowe ze składnika za pomocą metody instrumentacji, należy użyć [VSInstr.exe](../profiling/vsinstr.md) narzędzie, aby wygenerować instrumentowaną wersję składnika. Następnie uruchamiasz profiler. Po wykonaniu instrumentowanego składnika, dane chronometrażu są automatycznie zbierane do pliku danych. Można wstrzymywać i wznawiać zbieranie danych podczas sesji profilowania.  

 Aby zakończyć sesję profilowania, zamknij aplikację docelową i następnie jawnie Zamknij profiler.  

## <a name="start-the-profiling-session"></a>Rozpocznij sesję profilowania  

#### <a name="to-start-profiling-by-using-the-instrumentation-method"></a>Aby rozpocząć profilowanie za pomocą metody Instrumentacji  

1. Otwórz okno wiersza polecenia.  

2. Użyj **VSInstr** narzędzie do generowania instrumentowanej wersji aplikacji docelowej.  

3. Uruchom program profiler. Wpisz:  

    **/ OUTPUT polecenia VSPerfCmd:** `OutputFile` [`Options`]  

   - [/Start](../profiling/start.md)**: śledzenia** opcja inicjuje profiler.  

   - [/Output](../profiling/output.md)**:** `OutputFile` opcja jest wymagana przy użyciu **/start**. `OutputFile` Określa nazwę i lokalizację pliku danych (Vsp) profilowania.  

     Można użyć co najmniej jeden z następujących opcji z **polecenia** opcji.  

   | Opcja | Opis |
   | - | - |
   | [/ User](../profiling/user-vsperfcmd.md) **:**[`Domain`**\\**]`UserName` | Określa nazwę domeny i użytkownika konta, które jest właścicielem PROFILOWANEGO procesu. Ta opcja jest wymagana tylko wtedy, gdy proces działa jako użytkownik inny niż zalogowany użytkownik. Właściciel procesu jest wymieniony w **nazwa_użytkownika** kolumny na **procesy** kartę w Menedżerze zadań Windows. |
   | [/crosssession](../profiling/crosssession.md) | Włącza profilowanie procesów w innych sesjach. Ta opcja jest wymagana, jeśli aplikacja jest uruchomiona w innej sesji. Identyfikator sesji jest wymieniony w **identyfikator sesji** kolumny na karcie Procesy Menedżera zadań Windows. **Skróconej/CS** może być określona jako skrót **/crosssession**. |
   | [/globaloff](../profiling/globalon-and-globaloff.md) | Rozpoczyna się, które wstrzymana profilera ze zbieraniem danych. Użyj [globalon](../profiling/globalon-and-globaloff.md) Aby wznowić profilowanie. |
   | [/ Licznik](../profiling/counter.md) **:** `Config` | Zbiera informacje licznika wydajności procesora, który jest określony w `Config`. Informacje o liczniku jest dodawany do danych, które są zbierane podczas każdego zdarzenia profilowania. |
   | [/wincounter](../profiling/wincounter.md) **:** `WinCounterPath` | Określa licznik wydajności Windows mają być zbierane podczas profilowania. |
   | [/automark](../profiling/automark.md) **:** `Interval` | Za pomocą **/wincounter** tylko. Określa liczbę milisekund między zdarzeniami zbierania licznika wydajności Windows. Wartość domyślna to 500 ms. |
   | [/Events](../profiling/events-vsperfcmd.md) **:** `Config` | Określa zdarzenie śledzenie zdarzeń dla Windows (ETW) mają być zbierane podczas profilowania. Zdarzenia ETW są zbierane w osobnym (. *etl*) pliku. |


4. Uruchom aplikację docelową w typowy sposób.  

## <a name="control-data-collection"></a>Sterowanie zbieraniem danych  
 Gdy uruchomiona jest aplikacja docelowa, można kontrolować zbieranie danych przez uruchamianie i zatrzymywanie zapisywania danych do pliku za pomocą *VSPerfCmd.exe* opcje. Kontrolowanie zbierania danych umożliwia zbieranie danych dla określonej części wykonywania programu, takiej jak uruchamianie lub zamykanie aplikacji.  

#### <a name="to-start-and-stop-data-collection"></a>Aby uruchomić i zatrzymać zbieranie danych  

-   Następujące pary opcji uruchamiają i zatrzymują zbieranie danych. Określ każdą opcję w oddzielnym wierszu poleceń. Włączenie funkcji zbierania danych można włączać i wyłączać wiele razy.  

    |Opcja|Opis|  
    |------------|-----------------|  
    |[globalon /globaloff](../profiling/globalon-and-globaloff.md)|Uruchamia (**globalon**) lub zatrzymuje (**/globaloff**) zbieranie danych dla wszystkich procesów.|  
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|Uruchamia (**/processon**) lub zatrzymuje (**/processoff**) zbieranie danych dla procesu, który jest określony przez identyfikator procesu (`PID`).|  
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|Uruchamia (**/threadon**) lub zatrzymuje (**/threadoff**) zbieranie danych dla wątku, który jest określony przez identyfikator wątku (`TID`).|  

## <a name="end-the-profiling-session"></a>Kończenie sesji profilowania  
 Aby zakończyć sesję profilowania, zamknij aplikację, która działa składnik instrumentowany, a następnie wywołaj **VSPerfCmd** [/shutdown](../profiling/shutdown.md) opcję, aby wyłączyć profiler i zamknąć plik danych profilowania.  

#### <a name="to-end-a-profiling-session"></a>Aby zakończyć sesję profilowania  

1.  Zamknij aplikację docelową.  

2.  Zamknij program profilujący. Wpisz:  

     **Narzędzia VSPerfCmd/shutdown**  

## <a name="see-also"></a>Zobacz także  
 [Profil aplikacji autonomicznych](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Widok danych metody Instrumentacji](../profiling/instrumentation-method-data-views.md)