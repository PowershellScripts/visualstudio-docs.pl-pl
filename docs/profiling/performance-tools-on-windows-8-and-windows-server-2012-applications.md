---
title: "Narzędzia wydajności w przypadku aplikacji systemu Windows 8 i Windows Server 2012 | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 06/19/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a704215d-d252-4087-921b-ac81ebe2a9c9
caps.latest.revision: "15"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b6e71a7cc3200de9570ee0545bbc60e59943a693
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="performance-tools-on-windows-8-and-windows-server-2012-applications"></a>Narzędzia wydajności w przypadku aplikacji systemu Windows 8 i Windows Server 2012
Ulepszone funkcje zabezpieczeń w programie Windows 8 i Windows Server 2012 wymagane istotne zmiany w Visual Studio tools wydajności sposób zbierania danych na tych platformach. Aplikacje platformy uniwersalnej systemu Windows wymagają również nowe techniki kolekcji. W tym temacie opisano zmiany dotyczące narzędzi wydajności uruchamianie onWindows 8 i Windows Server 2012 platformy.
  
> [!NOTE]
>  Narzędzia wydajności dla innych obsługiwanych wersji systemu Windows (Windows 7, Windows Server 2008 R2) nie zostały zmienione.
  
##  <a name="BKMK_In_this_topic"></a>W tym temacie  
 [Zbieranie danych w aplikacji platformy uniwersalnej systemu Windows w środowisku IDE programu Visual Studio](#BKMK_Profiling_Windows_Store_apps_from_the_Visual_Studio_IDE)  
  
 [Zbieranie danych na aplikacje działające na pulpicie systemu Windows 8 lub Windows Server 2012 z programu Visual Studio IDE](#BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_from_the_Visual_Studio_IDE)  
  
-   [Zbieranie danych na aplikacje działające na pulpicie systemu Windows 8 lub Windows Server 2012 za pomocą próbkowania z programu Visual Studio IDE](#BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_by_using_sampling_from_the_Visual_Studio_IDE)  
  
 [Profilowanie z wiersza polecenia](#BKMK_Profiling_from_the_command_line)  
  
 [Zbieranie danych o interakcji między (TIP) warstwy](#BKMK_Collecting_tier_interaction__TIP__data)  
  
##  <a name="BKMK_Profiling_Windows_Store_apps_from_the_Visual_Studio_IDE"></a>Zbieranie danych w aplikacji platformy uniwersalnej systemu Windows w środowisku IDE programu Visual Studio  
 W przypadku profilu aplikacji platformy uniwersalnej systemu Windows, który jest zapisany w JavaScript i HTML 5, zbierania danych instrumentacji dla kodu JavaScript. Jeśli profil jest aplikacji platformy uniwersalnej systemu Windows lub składnik, który jest napisany w języku Visual C++, Visual C# lub Visual Basic, należy zebrać dane z próbkowania dla kodu natywnego i zarządzanego. Aplikację można profilu lokalnie lub na komputerze zdalnym.  
  
 Te funkcje profilowania i opcje nie są obsługiwane podczas profilowania aplikacji platformy uniwersalnej systemu Windows:  
  
-   Profilowanie aplikacji JavaScript za pomocą metody pobierania próbek.  
  
-   Profilowania kodu zarządzanego i natywnego przy użyciu metody instrumentacji.  
  
-   Profilowania współbieżności  
  
-   Profilowania pamięci .NET  
  
-   Interakcja warstwowa profilowania (TIP)  
  
-   Opcje próbkowania, takie jak ustawianie zdarzenie próbkowania i interwał czasu lub zbieranie danych licznika wydajności.  
  
-   Opcje instrumentacji, takie jak zbieraniem danych dotyczących wydajności oraz danych liczników systemu windows lub określ dodatkowe opcje wiersza polecenia.  
  
 Aby uzyskać więcej informacji na temat profilowania aplikacji platformy uniwersalnej systemu Windows zobacz następujące tematy:  
  
 [Uruchamianie aplikacji platformy uniwersalnej systemu Windows na komputerze lokalnym](../debugger/run-windows-store-apps-on-the-local-machine.md)  
  
 [Uruchamianie aplikacji platformy uniwersalnej systemu Windows na komputerze zdalnym](../debugger/run-windows-store-apps-on-a-remote-machine.md)  
  
 [Narzędzia profilowania](profiling-tools.md)  
  
-   [Pamięć języka JavaScript](../profiling/javascript-memory.md)
  
-   [Kod profil Visual C++, Visual C# i Visual Basic w aplikacjach platformy uniwersalnej systemu Windows na komputerze lokalnym](http://msdn.microsoft.com/en-us/2d0c939e-0bac-48c5-b727-46f6c6113060)  
  
-   [Kod profil Visual C++, Visual C# i Visual Basic w aplikacjach platformy uniwersalnej systemu Windows na urządzeniu zdalnym](http://msdn.microsoft.com/en-us/b932a2be-11b0-40fd-b996-75c6b6a79d22)  
  
-   [Analizowanie danych dotyczących wydajności dla kodu Visual C++, Visual C# i Visual Basic w aplikacjach platformy uniwersalnej systemu Windows](http://msdn.microsoft.com/en-us/5de4a413-d924-425f-afc4-e1ecfb0fca18)  
  
 [W tym temacie](#BKMK_In_this_topic)  
  
##  <a name="BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_from_the_Visual_Studio_IDE"></a>Zbieranie danych na aplikacje działające na pulpicie systemu Windows 8 lub Windows Server 2012 z programu Visual Studio IDE  
 Profilowanie przy użyciu metody Instrumentacji nie została zmieniona dla systemu Windows 8.  
  
 Interakcja warstwowa profilowania (TIP) nie jest obsługiwana przy użyciu metody próbkowania.  
  
###  <a name="BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_by_using_sampling_from_the_Visual_Studio_IDE"></a>Zbieranie danych na aplikacje działające na pulpicie systemu Windows 8 lub Windows Server 2012 za pomocą próbkowania z programu Visual Studio IDE  
 Te funkcje profilowania i opcje nie są obsługiwane podczas profilowania aplikacji klasycznych systemu Windows 8 lub przy użyciu metody próbkowania aplikacji systemu Windows Server 2012:
  
-   Interakcja warstwowa profilowania (TIP). Zbieranie danych o PORADĘ jest obsługiwana za pomocą Instrumentacji.
  
-   Próbkowanie opcje, takie jak ustawianie zdarzenie próbkowania i interwał czasu lub zbieranie danych licznika wydajności.  
  
##  <a name="BKMK_Profiling_from_the_command_line"></a>Profilowanie z wiersza polecenia  
 Dwa narzędzia wiersza polecenia służy do zbierania danych profilowania na urządzeniach z systemem Windows 8 i Windows Server 2012, w tym urządzeń, które nie mają instalację programu Visual Studio:  
  
|Nazwa narzędzia|Opis|  
|---------------|-----------------|  
|[VSPerf](../profiling/vsperf.md)|Zbiera dane profilowania z aplikacji platformy uniwersalnej systemu Windows i zbiera dane profilowania przykładowej aplikacji klasycznych systemu Windows 8 i Windows Server 2012 aplikacji...|  
|[VSPerfCmd](../profiling/vsperfcmd.md)|Zbiera dane instrumentacji, współbieżności i interakcja warstwowa profilowania danych z aplikacji, które są uruchomione na pulpicie theWindows 8 lub Windows Server 2012. Zbiera dane profilowania z poprzednich wersji systemu Windows.|  
  
 Zarówno narzędzia są zainstalowane z programem Visual Studio do użytku na komputerze lokalnym.  
  
 Do profilu aplikacji na urządzeniach, które nie mają zainstalowanego, programu Visual Studio wykonaj jedną z następujących czynności:  
  
-   Pobierz narzędzia jako część narzędzi Remote Tools for Visual Studio z [witryny sieci web MSDN](http://go.microsoft.com/fwlink/?LinkID=219549).  
  
-   Kopiowanie i uruchom program instalacyjny narzędzia Autonomiczny profilera z komputera programu Visual Studio. Programy instalacyjne znajdują się w *VSInstallDir %* **\Team Tools\Performance Tools\Setups** folderu. Wybierz Instalatora systemu operacyjnego (x86/x64) komputera zdalnego.  
  
> [!NOTE]
>  Aby zbierać dane profilowania PORADĘ, musi instalowanie autonomiczny profilera z komputera program Visual Studio na komputerze zdalnym.  
  
 Te funkcje profilowania i opcje nie są obsługiwane podczas profilowanie aplikacji Windows 8 i Windows Server 2012 w wierszu polecenia:  
  
-   Zbieranie danych z aplikacji sieci web systemu Windows 8 i Windows Server 2012 przy użyciu trybu próbkowania z [VSPerfASPNetCmd](../profiling/vsperfaspnetcmd.md).  
  
-   Zbieranie danych pobierania próbek przy użyciu VsPerfCmd.exe.  
  
-   Próbkowanie opcje, takie jak ustawianie zdarzenie próbkowania i interwał czasu lub zbieranie danych licznika wydajności.  
  
##  <a name="BKMK_Collecting_tier_interaction__TIP__data"></a>Zbieranie danych o interakcji między (TIP) warstwy  
 Profilowanie interakcji między warstwami udostępnia dodatkowe informacje o czas wykonywania funkcji aplikacji wielowarstwowych, które komunikują się z bazami danych za pośrednictwem usług ADO.NET. Dane są zbierane tylko dla wywołań synchronicznych funkcji.  
  
 **Wersje Visual Studio**  
  
 Interakcja warstwowa profilowania danych mogą być zbierane przy użyciu [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)], [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)], lub [!INCLUDE[vs_pro_current_short](../profiling/includes/vs_pro_current_short_md.md)]. Jednak interakcja warstwowa profilowania danych jest możliwy tylko w [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)] i [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)].  
  
 **Windows 8 i Windows Server 2012**  
  
1.  Do zbierania danych o interakcji między warstwy z aplikacji, które są uruchomione na pulpicie systemu Windows 8 lub Windows Server 2012, należy użyć metody instrumentacji.  
  
2.  Nie można zebrać danych o interakcji między warstwy dla aplikacji platformy uniwersalnej systemu Windows.  
  
3.  Warstwa danych o interakcji między mogą obejmować wszystkie metody profilowania w innej wersji systemu Windows.  
  
 **Kreator wydajności i Eksplorator wydajności**  
  
 W Eksploratorze wydajności, należy dodać opcję zbierania danych interakcji warstwy do uruchomienia profilowania. Należy również dodać projekt, plik wykonywalny lub witryny sieci Web do węzła docelowego Eksplorator wydajności. Zobacz [zbierania danych o interakcji między warstwy](../profiling/collecting-tier-interaction-data.md).  
  
 **Zbieranie danych Porada na komputerze zdalnym**  
  
 Do zbierania danych o interakcji między warstwy komputera zdalnego, należy skopiować **vs_profiler_***\<platformy >***_**  *\< Język >***.exe** plik z *VSInstallDir %***\Team Tools\Performance Tools\Setups** folderu maszyny do programu Visual Studio komputer zdalny i zainstaluj go. Nie można użyć narzędzi profilowania w [zdalnego debugowania](../debugger/remote-debugging.md) Pobierz pakiet.  
  
 Można użyć [VSPerfCmd](../profiling/vsperfcmd.md) lub [VSPerfASPNetCmd](../profiling/vsperfaspnetcmd.md) do zbierania danych profilowania.  
  
 **Porada raportów**  
  
 Warstwa danych o interakcji między mogą być przeglądane tylko w [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)] lub [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)] IDE. Interakcja warstwowa plikowym raportów za pośrednictwem [VSPerfReport](../profiling/vsperfreport.md) nie są dostępne.  
  
## <a name="see-also"></a>Zobacz też  
 [Eksplorator wydajności](../profiling/performance-explorer.md)   
 [Konfigurowanie sesji wydajności](../profiling/configuring-performance-sessions.md)   
 [Profilowanie z wiersza polecenia](../profiling/using-the-profiling-tools-from-the-command-line.md)