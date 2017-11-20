---
title: "Porady: dołączanie profilera do natywnej autonomicznej aplikacji i zbieranie danych współbieżności przy użyciu wiersza polecenia | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 12d3e0f3-4b74-4e66-8fbf-8ac99bd4f91c
caps.latest.revision: "22"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4202530fd58f1a3323284cd3c7e59e36ba7b2a8f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-attach-the-profiler-to-a-native-stand-alone-application-and-collect-concurrency-data-by-using-the-command-line"></a>Porady: dołączanie profilera do natywnej aplikacji autonomicznej i zbieranie danych współbieżności przy użyciu wiersza polecenia
W tym temacie opisano sposób użycia [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] narzędzia wiersza polecenia narzędzi profilowania dołączanie profilera do aplikacji autonomicznej uruchomiona natywnego (C/C++) i zbierać z wątku danych rywalizacji.  
  
> [!NOTE]
>  Narzędzia wiersza polecenia narzędzi profilowania znajdują się w podkatalogu narzędzia \Team Tools\Performance katalogu instalacyjnego programu Visual Studio. Na komputerach 64-bitowych zarówno 64-bitowe i 32-bitowe wersje narzędzia są dostępne. Aby użyć narzędzia wiersza polecenia profilera, należy dodać ścieżkę do narzędzia do zmiennej środowiskowej PATH z **wiersza polecenia** okna lub dodaj je do samo polecenie. Aby uzyskać więcej informacji, zobacz [Określanie ścieżki do narzędzi wiersza polecenia](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
  
 Profiler jest dołączony do aplikacji, można wstrzymywać i wznawiać zbierania danych. Aby zakończyć sesję profilowania, profilera nie musi być dołączony do aplikacji i profilera muszą zostać jawnie wyłączone.  
  
## <a name="attaching-the-profiler-to-a-running-native-application"></a>Dołączanie profilera do aplikacji natywnej uruchomiona  
  
#### <a name="to-attach-the-profiler-to-a-running-native-application"></a>Aby dołączanie profilera do aplikacji natywnej uruchomiona  
  
1.  W wierszu polecenia wpisz następujące polecenie:  
  
     [VSPerfCmd](../profiling/vsperfcmd.md) **/start:concurrency**  
  
     Można użyć tych opcjach w poniższej tabeli z **/start:concurrency**opcji.  
  
    |Opcja|Opis|  
    |------------|-----------------|  
    |[/ User](../profiling/user-vsperfcmd.md) **:**[`Domain\`]`Username`|Określa opcjonalne domenę i nazwę użytkownika konta, aby uzyskać dostęp do profilera.|  
    |[/ crosssession](../profiling/crosssession.md)|Włącza profilowanie procesów w innych sesji logowania.|  
    |[/wincounter](../profiling/wincounter.md) **:**`WinCounterPath`|Określa licznik wydajności systemu Windows, które będą zbierane podczas profilowania.|  
    |[/automark](../profiling/automark.md) **:**`Interval`|Za pomocą **/wincounter** tylko. Określa liczbę milisekund między zdarzeniami kolekcji liczników wydajności systemu Windows. Wartość domyślna to 500.|  
    |[/Events](../profiling/events-vsperfcmd.md) **:**`Config`|Określa zdarzenia funkcji Śledzenie zdarzeń systemu Windows (), które mają być zbierane podczas profilowania. Zdarzenia ETW są gromadzone w pliku oddzielne (ETL).|  
  
2.  Dołączanie profilera do aplikacji docelowej, wpisując następujące polecenie:  
  
     **VSPerfCmd**[/ dołączyć](../profiling/attach.md) **:**{`PID`&#124;`ProcName`}    
  
     `PID`Określa identyfikator procesu aplikacji docelowej. Identyfikatory wszystkich procesów uruchomionych procesów można wyświetlić w Menedżerze zadań systemu Windows.  
  
## <a name="controlling-data-collection"></a>Kontrolowanie zbierania danych  
 Aplikacja docelowa jest uruchomiona, można kontrolować zbierania danych przez uruchamianie i zatrzymywanie przy zapisywaniu danych do pliku przy użyciu opcji VSPerfCmd.exe. Przez kontrolowanie zbierania danych może zbierać dane dotyczące określonych części wykonania programu, takie jak uruchamianie lub zamykanie aplikacji.  
  
#### <a name="to-start-and-stop-data-collection"></a>Aby uruchomić i zatrzymać zbieranie danych  
  
-   Pary opcje w poniższej tabeli uruchomić i zatrzymać zbieranie danych. Określ opcję każdego w osobnym wierszu polecenia. Włączenie funkcji zbierania danych można włączać i wyłączać wiele razy.  
  
    |Opcja|Opis|  
    |------------|-----------------|  
    |[/globalon /globaloff](../profiling/globalon-and-globaloff.md)|Uruchamia (**/globalon**) lub zatrzymania (**/globaloff**) zbierania danych dla wszystkich procesów.|  
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:**`PID`|Uruchamia (**/processon**) lub zatrzymania (**/processoff**) zbierania danych przez proces który identyfikator procesu (`PID`) określa.|  
    |[/ dołączyć](../profiling/attach.md) **:**{`PID`&#124;`ProcName`} [/ detach](../profiling/detach.md)[**:**{`PID`&#124;`ProcName`}]|**/ dołączyć** rozpoczyna zbieranie danych przez proces który identyfikator procesu (`PID`) lub nazwa procesu (*Nazwa_procedury*) określa. **/ detach** zatrzymuje zbieranie danych dla określonego procesu lub dla wszystkich procesów, jeśli jest określony żaden proces.|  
  
## <a name="ending-the-profiling-session"></a>Kończenie sesji profilowania  
 Aby zakończyć sesję profilowania, profilera musi nie być zbierania danych. Można zatrzymać zbieranie danych z aplikacji, która jest profilowane za pomocą metody pobierania próbek przez zamknięcie aplikacji lub wywoływania **VSPerfCmd / detach** opcji. Następnie wywołaj **VSPerfCmd/shutdown** opcję, aby wyłączyć profilera i zamknij plik danych profilowania.  
  
#### <a name="to-end-a-profiling-session"></a>Aby zakończyć sesję profilowania  
  
1.  Odłączanie profilera z aplikacji docelowej, jej zamknięcie lub wpisując następujące polecenie:  
  
     **VSPerfCmd / detach**  
  
2.  Zamknij profilera, wpisując następujące polecenie:  
  
     **VSPerfCmd** [ /shutdown  ](../profiling/shutdown.md)