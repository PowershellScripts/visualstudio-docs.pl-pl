---
title: Uruchamianie sesji debugowania dla aplikacji platformy uniwersalnej systemu Windows w programie Visual Studio | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/04/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- VC.Project.IVCAppHostRemoteDebugPageObject.MachineName
- VC.Project.IVCAppHostRemoteDebugPageObject.BreakpointBehavior
- VC.Project.IVCAppHostLocalDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCAppHostTetheredDebugPageObject.DebuggerType
- VC.Project.IVCAppHostLocalDebugPageObject.BreakpointBehavior
- VC.Project.IVCAppHostRemoteDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostRemoteDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCAppHostLocalDebugPageObject.DebuggerType
- VC.Project.IVCAppHostSimulatorDebugPageObject.DebuggerType
- ImmersiveProjects.Properties.Debug
- VC.Project.IVCAppHostTetheredDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostSimulatorDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostSimulatorDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCAppHostLocalDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostLocalDebugPageObject.AllowLocalNetworkLoopback
- AppPackage.Properties.Debug
- VC.Project.IVCAppHostRemoteDebugPageObject.Authentication
- VC.Project.IVCAppHostRemoteDebugPageObject.DebuggerType
- VC.Project.IVCAppHostSimulatorDebugPageObject.BreakpointBehavior
- vs.debug.installedapppackagelauncher
- vs.debug.error.wwahost_scriptdebuggingdisabled
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- uwp
ms.openlocfilehash: a7a9f74450ccf2cb493e44fa1fecef0630a27569
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49818787"
---
# <a name="start-a-debugging-session-for-a-uwp-app-in-visual-studio"></a>Uruchamianie sesji debugowania dla aplikacji platformy uniwersalnej systemu Windows w programie Visual Studio
  
 W tym temacie opisano sposób uruchamiania sesji debugowania dla aplikacji platformy uniwersalnej systemu Windows w XAML i program Visual C++, Visual C#, lub Visual Basic, a w przypadku aplikacji platformy uniwersalnej systemu Windows zapisywane w kodzie HTML i JavaScript. Debugowanie aplikacji obejmuje zarówno Konfigurowanie sesji debugowania, jak i wybierając sposób, aby uruchomić aplikację.  
  
##  <a name="BKMK_The_easy_way_to_start_debugging"></a> Prosty sposób Rozpocznij debugowanie  
  
1. Otwórz rozwiązanie aplikacji w programie Visual Studio.  
  
2. Wybierz F5.  
  
   Visual Studio kompiluje i uruchamia aplikację w debugerze. Wykonywanie jest kontynuowane, dopóki punkt przerwania zostanie osiągnięty, ręcznie zawieszenie wykonywania, wystąpi nieobsługiwany wyjątek, lub kończy się w aplikacji.  
  
##  <a name="BKMK_Choose_the_build_configuration_options"></a> Wybór opcji konfiguracji kompilacji  
  
1.   Z listy rozwijanej obok pozycji listy **Rozpocznij debugowanie** przycisk na debuger **standardowa** narzędzi, wybierz **debugowania**.  
  
2.  Z **platformy** listy wybierz platformę docelową kompilacji dla.  
  
##  <a name="BKMK_Choose_the_deployment_target"></a> Wybierz cel wdrożenia  
  
Można wdrażać i debugować aplikację platformy uniwersalnej systemu Windows na komputerze programu Visual Studio, podłączonego urządzenia, symulatorze programu Visual Studio na komputerze lokalnym, urządzenie zdalne lub emulator. Wybierz cel wdrożenia z listy rozwijanej z prawej strony **platformy** obiektu docelowego debugera **standardowa** paska narzędzi.
  
![Wybierz cel wdrożenia](../debugger/media/vsrun_select_target_device.png)  
  
Wybierz jedną z następujących opcji:  
  
|||  
|-|-|  
|**Maszyna lokalna**|Debugowanie aplikacji w bieżącej sesji na komputerze lokalnym.|  
|**Symulator**|Debugowanie aplikacji w symulatorze programu Visual Studio dla aplikacji platformy uniwersalnej systemu Windows. Symulator jest oknem pulpitu, które umożliwia debugowanie funkcji urządzeniami — takich jak gestów dotykowych i obracanie urządzeń — które mogą nie być dostępne na komputerze lokalnym. Ta opcja jest dostępna tylko jeśli Twoja aplikacja **minimalnej platformy docelowej. Wersja** jest mniejsza niż system operacyjny na komputerze deweloperskim. Zobacz [uruchamianie aplikacji platformy UWP w symulatorze](../debugger/run-windows-store-apps-in-the-simulator.md).|  
|**Komputer zdalny**|Debugowanie aplikacji na urządzeniu, do którego jest podłączony do komputera lokalnego za pośrednictwem intranetu lub podłączone bezpośrednio za pomocą kabla Ethernet. Zdalne debugowanie Remote Tools for Visual Studio musi być zainstalowana i uruchomiona na urządzeniu zdalnym. Zobacz [uruchamianie aplikacji platformy UWP na komputerze zdalnym](../debugger/run-windows-store-apps-on-a-remote-machine.md).|  
|**urządzenia**|Debugowanie aplikacji na urządzeniu z portu USB. Urządzenie musi być odblokowany i mają ekranu odblokowane.|  
|**Mobile Emulator**|Rozruch konfiguracja określona w nazwie emulator emulator, Wdróż aplikację i Rozpocznij debugowanie. Emulatory są dostępne tylko na komputerach z włączoną funkcją Hyper-V.|  

##  <a name="BKMK_Open_the_debugging_property_page_for_the_project"></a> Wybierz dodatkowe opcje debugowania  

Jeśli potrzebujesz skonfigurować dodatkowe opcje debugowania, należy otworzyć stronę właściwości dla projektu.
  
1.  W Eksploratorze rozwiązań wybierz projekt. W menu skrótów wybierz **właściwości**.  
  
2.  To zrobić, aby otworzyć stronę właściwości debugowania dla projektu:  
  
    -   W przypadku aplikacji języka Visual C# i Visual Basic, wybierz **debugowania**.  
  
         ![C&#35; &#47; strony właściwości debugowania projektu VB](../debugger/media/dbg_csvb_debugpropertypage.png)  
  
    -   W przypadku aplikacji Visual C++ i JavaScript, rozwiń węzeł **właściwości konfiguracji** węzeł, a następnie wybierz **debugowanie**.  
  
         ![C&#43; &#43; debugowania strona właściwości aplikacji platformy uniwersalnej systemu Windows](../debugger/media/dbg_cpp_debugpropertypage.png)  

###  <a name="BKMK_Choose_the_debugger_to_use"></a> Wybierz debuger do użycia  
Domyślnie program Visual Studio debugować kodu zarządzanego w aplikacjach języka C# i Visual Basic. W przypadku aplikacji C# i Visual Basic można debugować zarówno zarządzanego i natywnego kodu C/C++ w aplikacji. W aplikacjach C++ Visual Studio debuguje kodu natywnego, domyślnie. W aplikacji JavaScript programu Visual Studio debugować skrypt domyślnie. 
  
Dla aplikacji C++ i JavaScript można debugować określone typy kodu, które znajdują się w części aplikacji zamiast lub oprócz kodu natywnego. Określ kod do debugowania **typ debugera** listy na **debugowanie** strony właściwości projektu aplikacji.  
  
Wybierz jedną z tych debugerów z **proces aplikacji** listy:  
  
|||  
|-|-|  
|**Tylko zarządzany**|Debugowanie kodu zarządzanego w aplikacji. Kod języka JavaScript i kodu natywnego języka C/C++ są ignorowane.|  
|**Tylko w trybie macierzystym**|Debugowanie kodu natywnego języka C/C++ w aplikacji. Kod zarządzany i kod JavaScript są ignorowane.|  
|**Mieszany (zarządzany i natywny)**|Debugowanie kodu C/C++ natywnego i zarządzanego kodu w aplikacji. Kod JavaScript jest ignorowany. W projektach C++, ta opcja jest wywoływana **(zarządzany i natywny)**.|  
|**Jenom skript**|Debugowanie kodu JavaScript w aplikacji. Kodu zarządzanego i natywnego kodu są ignorowane.|  
|**Skrypt i natywny**|Debugowanie kodu natywnego języka C/C++ oraz kodu JavaScript w aplikacji. Kod zarządzany jest ignorowany. Dostępne w tylko dla projektów C++.|  
|**Tylko procesor GPU (C++ AMP)**|Debugowanie kodu natywnego języka C++ jest uruchamiany na jednostka przetwarzania grafiki (GPU). Dostępne w tylko dla projektów C++.|  

W C# i aplikacji w języku Visual Basic, możesz również ustawić taki sam **typ debugera** wartości dla dowolnego zadania w tle, które są częścią projektu.
  
###  <a name="BKMK__Optional__Delay_starting_the_debug_session"></a> (Opcjonalnie) Opóźnienie uruchamiania sesji debugowania  
 Domyślnie program Visual Studio natychmiast uruchamia aplikację po rozpoczęciu debugowania. Można również uruchomić sesję debugowania, ale opóźnić uruchomienie aplikacji. Po wybraniu tej opcji, aplikacja jest uruchomiona w debugerze po uruchomieniu na ekranie startowym lub umowy o aktywacji, lub gdy jest uruchomiona przez inny proces lub metody. Jeśli chcesz debugować zadanie w tle, gdy aplikacja nie jest uruchomiony, również opóźnić uruchomienie aplikacji.  
  
 Aby opóźnić uruchomienie aplikacji, możesz wykonywać następujące czynności:  
  
-   W przypadku aplikacji języka Visual C# i Visual Basic, wybierz **nie uruchamiaj, ale Debuguj kod przy rozpoczęciu** na **debugowania** stronę właściwości.  
  
-   W przypadku aplikacji Visual C++ i JavaScript, wybierz **nie** z **Uruchom aplikację** listy na **debugowanie** stronę właściwości.  
  
###  <a name="BKMK__Optional__Disable_network_loopbacks"></a> (Opcjonalnie) Wyłącz sprzężenia zwrotne sieci  
  
 Ze względów bezpieczeństwa aplikacji platformy UWP, który jest zainstalowany w sposób standardowy jest niedozwolone wykonywania wywołań sieci do zainstalowania na urządzeniu. Domyślnie wdrożenie programu Visual Studio tworzy wyjątek od tej reguły dla wdrożonej aplikacji. To wykluczenie umożliwia przetestowanie procedur komunikacji na jednym komputerze. Przed przesłaniem aplikacji do Microsoft Store, należy przetestować aplikację bez zwolnienia.  
  
 Aby usunąć wykluczenie sprzężenie zwrotne sieci:  
  
-   Wizualizacji C# i aplikacji Visual Basic, wyczyść **Zezwalaj na sprzężenie zwrotne sieci lokalnej** pole wyboru na **debugowania** stronę właściwości.  
  
-   W przypadku aplikacji Visual C++ i JavaScript, wybierz **nie** z **Zezwalaj na sprzężenie zwrotne lokalnej sieci** listy na **debugowanie** stronę właściwości.  
  
###  <a name="BKMK__Optional__Reinstall_the_app_when_you_start_debugging"></a> (Opcjonalnie) Ponownie zainstaluje aplikację po rozpoczęciu debugowania  
 Diagnozowanie problemów z instalacji i wstępnej konfiguracji aplikacji języka Visual C# lub Visual Basic, wybierz **Odinstaluj i ponownie zainstaluj Mój pakiet** na **debugowania** stronie właściwości, aby odtworzyć oryginalnej instalacji podczas uruchamiania debugowania. Ta opcja nie jest dostępne dla projektów Visual C++ i JavaScript.  
  
###  <a name="BKMK__Optional__Disable_authentication_requirement_to_start_the_remote_debugger"></a> (Opcjonalnie) Wyłączyć wymaganie uwierzytelniania można uruchomić debugera zdalnego  
  
 Domyślnie, należy podać poświadczenia, aby uruchomić zdalny debuger po wybraniu **maszyny zdalnej** jako cel wdrożenia.
  
> [!IMPORTANT]
>  Istnieje możliwość uruchomienia zdalnego debugera bez uwierzytelniania, ale używanie tego trybu jest zdecydowanie odradzane. Po uruchomieniu w tym trybie nie ma zabezpieczeń sieci. Wybierz pozycję bez uwierzytelniania tylko wtedy, gdy masz pewność, że sieć nie jest narażone złośliwego kodu lub szkodliwy ruch.  
  
 Aby usunąć wymaganie uwierzytelniania:  
  
1.  Wizualizacji C# i aplikacji Visual Basic, wybierz opcję **maszyny zdalnej** jako **urządzenie docelowe** na **debugowania** strony właściwości, a następnie ustaw **uwierzytelniania Tryb** do **Brak** lub **uniwersalny (protokół niezaszyfrowanym)**.
  
2.  W przypadku aplikacji Visual C++ i JavaScript, wybierz **maszyny zdalnej** jako **urządzenie docelowe** na **debugowanie** strony właściwości, a następnie ustaw **wymagają Uwierzytelnianie** do **Brak** lub **uniwersalny (protokół niezaszyfrowanym)**.  

    **Uniwersalny (protokół niezaszyfrowanym)** jest przeznaczona do użytku w przypadku wdrażania na urządzeniu zdalnym. Obecnie dotyczy to urządzeń IoT, urządzenia Xbox i urządzenia HoloLens, a także aktualizacja dla twórców lub nowszej komputerów z systemem. Uniwersalny (protokół niezaszyfrowanym) można używać tylko w sieciach zaufanych. Połączenie debugowania jest narażony na złośliwych użytkowników, którzy mogą przechwytywać i zmiany danych są przekazywane między środowiskami deweloperskim i komputera zdalnego.  
  
##  <a name="BKMK_Start_the_debugging_session"></a> Rozpocznij sesję debugowania  
  
###  <a name="BKMK_Start_debugging__F5_"></a> Rozpocznij debugowanie (F5)  
 Po wybraniu **Rozpocznij debugowanie** (klawiatura: F5) na **debugowania** menu programu Visual Studio uruchamia aplikację w debugerze. Wykonywanie jest kontynuowane, dopóki nie zostanie osiągnięty punkt przerwania, ręcznie zawieszenie wykonywania, wystąpi wyjątek, lub aplikacja kończy się.  
  
###  <a name="BKMK_Start_debugging__F5__but_delay_the_app_start"></a> Rozpocznij debugowanie (F5), ale opóźnić uruchomienie aplikacji  
 Możesz ustawić aplikację, aby uruchomić tryb debugowania, ale początek metody innej niż debugera. Na przykład możesz zechcieć, debugowanie, uruchamianie aplikacji z Start menu lub debugować proces w tle w aplikacji bez uruchamiania aplikacji. Aby opóźnić uruchomienie aplikacji, wykonaj następujące czynności:  
  
- Na **debugowania** strona właściwości aplikacji (**debugowanie** w języku Visual C++ i JavaScript)  
  
  -   W przypadku aplikacji języka Visual C# i Visual Basic, wybierz **nie uruchamiaj, ale Debuguj kod przy rozpoczęciu**.  
  
  -   W przypadku aplikacji Visual C++ i JavaScript, wybierz **tak** z **Uruchom aplikację** listy.  
  
- Wybierz **Rozpocznij debugowanie** na **debugowania** menu (klawiatura: F5).  
  
- Rozpocznij tworzenie aplikacji z menu Start, kontrakt wykonywania lub innej procedury.  
  
  Aplikacja uruchamia się w trybie debugowania. Wykonywanie jest kontynuowane, dopóki punkt przerwania zostanie osiągnięty, ręcznie zawieszenie wykonywania, wystąpi nieobsługiwany wyjątek, lub kończy się w aplikacji.  
  
  Aby uzyskać więcej informacji na temat debugowania zadania w tle, zobacz [wyzwalacza wstrzymania, wznowienia i zdarzeń aplikacji platformy UWP w tle)](../debugger/how-to-trigger-suspend-resume-and-background-events-for-windows-store-apps-in-visual-studio.md).  
  
###  <a name="BKMK_Start_an_installed_app_in_the_debugger"></a> Uruchom zainstalowaną aplikację w debugerze  
Po rozpoczęciu debugowania przy użyciu klawisza F5, Visual Studio tworzy aplikacja jest wdrażana, ustawia aplikację do uruchamiania w trybie debugowania i następnie rozpoczyna się. Aby uruchomić aplikację, która jest już zainstalowana na urządzeniu, należy użyć **pakietu debugowania zainstalowanej aplikacji** okno dialogowe. Ta procedura jest przydatne, gdy trzeba debugować aplikację, która została zainstalowana z Microsoft Store lub w przypadku, gdy masz pliki źródłowe dla aplikacji, ale nie masz projektu programu Visual Studio dla aplikacji. Na przykład Niewykluczone, że system kompilacji niestandardowej, która nie korzysta z programu Visual Studio projektów i rozwiązań.  
  
Aplikację można zainstalować na urządzeniu lokalnym lub można go na urządzeniu zdalnym.  Aplikację można rozpocząć natychmiast, lub można ustawić go do uruchamiania w debugerze, gdy jest uruchomiona przez inny proces lub metody, np. w menu Start lub przez kontrakt aktywacji, można również ustawić aplikacji do uruchamiania w trybie debugowania, gdy chcesz debugować proces w tle bez uruchamiania aplikacji. Aby uzyskać więcej informacji, zobacz [wyzwalacza wstrzymania, wznowienia i zdarzeń aplikacji platformy UWP w tle)](../debugger/how-to-trigger-suspend-resume-and-background-events-for-windows-store-apps-in-visual-studio.md).  
  
Aby uruchomić zainstalowanej aplikacji w debugerze, wybierz **debugowania**, następnie **inne cele debugowania**, a następnie **pakietu debugowania zainstalowanej aplikacji**. Aby uzyskać dodatkowe instrukcje, zobacz [debugowanie zainstalowanego pakietu aplikacji](../debugger/debug-installed-app-package.md).

###  <a name="BKMK_Attach_the_debugger_to_a_running_app_"></a> Dołącz debuger do uruchomionej aplikacji platformy uniwersalnej systemu Windows  

Aby debugować uruchomionej aplikacji platformy uniwersalnej systemu Windows, wybierz **debugowania**, następnie **inne cele debugowania**, a następnie **pakietu debugowania zainstalowanej aplikacji**. Aby uzyskać dodatkowe instrukcje, zobacz [debugowanie zainstalowanego pakietu aplikacji](../debugger/debug-installed-app-package.md).
  
###  <a name="BKMK_Attach_the_debugger_to_a_running_app_"></a> Dołącz debuger do uruchomionej aplikacji Windows 8.x
 Aby dołączyć debuger [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] aplikacji, musisz podać Debugowalny Menedżer pakietów do zestawu aplikacji do uruchamiania w trybie debugowania. Debugowalny Menedżer pakietów jest zainstalowany za pomocą narzędzi Remote Tools for Visual Studio.  
  
 Dołączanie debugera do aplikacji jest przydatne, gdy potrzebujesz debugować aplikację już zainstalowane, takie jak aplikacja, która została zainstalowana z [!INCLUDE[win8_appstore_long](../debugger/includes/win8_appstore_long_md.md)]. Dołączanie jest wymagany w przypadku, gdy masz pliki źródłowe dla aplikacji, ale nie masz projektu programu Visual Studio dla aplikacji. Na przykład Niewykluczone, że system kompilacji niestandardowej, która nie korzysta z programu Visual Studio projektów i rozwiązań.  
  
 Dołączanie debugera do aplikacji wymaga wykonania tych kroków:  
  
1.  Ustaw aplikację do uruchamiania w trybie debugowania. Jest to niezbędne, gdy aplikacja nie jest uruchomiona.  
  
2.  Uruchom aplikację. Aplikację można uruchomić z ekranu startowego, kontrakt wykonywania lub innej metody.  
  
3.  Dołącz debuger do uruchomionej aplikacji.  
  
####  <a name="BKMK_Set_the_app_to_run_in_debug_mode"></a> Ustaw aplikację do uruchamiania w trybie debugowania  
  
1.  Instalowanie narzędzi Remote Tools dla programu Visual Studio na urządzeniu, w którym aplikacja zostanie zainstalowana. Zobacz [Instalowanie narzędzi zdalnych](../debugger/remote-debugging.md).  
  
2.  Na ekranie startowym Wyszukaj `Debuggable Package Manager` , a następnie uruchom go.  
  
     Zostanie wyświetlone okno programu PowerShell, poprawnie skonfigurowany na potrzeby polecenia cmdlet AppxDebug.  
  
3.  Aby włączyć debugowanie aplikacji, należy określić identyfikator element PackageFullName aplikacji. Aby wyświetlić listę wszystkich aplikacji, które zawiera element PackageFullName, wpisz `Get-AppxPackage` w wierszu polecenia programu PowerShell.  
  
4.  W wierszu polecenia programu PowerShell wprowadź `Enable-AppxDebug` *Pełna_nazwa_pakietu* gdzie *Pełna_nazwa_pakietu* jest identyfikatorem element PackageFullName aplikacji.  
  
####  <a name="BKMK_Attach_the_debugger"></a> Dołącz debuger  
 Aby dołączyć debuger:  
  
1. Na **debugowania** menu, wybierz **dołączyć do procesu**.  
  
    **Dołączyć do procesu** pojawi się okno dialogowe.  
  
2. Aby dołączyć do aplikacji na urządzeniu zdalnym, należy określić urządzenie zdalne w **kwalifikator** pole. Można:  
  
   -   Wprowadź nazwę w **kwalifikator** pole.  
  
   -   Wybierz strzałkę w dół w **kwalifikator** pole, a następnie wybierz urządzenie z listy urządzeń dołączonych do przed.  
  
   -   Wybierz **znaleźć** do wybierz urządzenie z listy urządzeń w danej podsieci lokalnej.  
  
3. Określ typ kodu, który chcesz debugować w **dołączyć do** pola.  
  
    Wybierz **wybierz** , a następnie wykonaj jedną z następujących czynności:  
  
   -   Wybierz **automatycznie Określ typ kodu do debugowania**  
  
   -   Wybierz **debugowania tych typów kodu** a następnie wybierz jeden lub więcej typów z listy.  
  
4. W **dostępne procesy** wybierz proces aplikacji.  

   > [!NOTE]
   >  W przeciwieństwie do innych typów aplikacji JavaScript aplikacje uruchomione w wystąpienie procesu wwahost.exe. Innym aplikacjom JavaScript są uruchomione po dołączeniu do aplikacji, musisz jest znany identyfikator liczbowych procesu (PID) wwahost.exe działający w aplikacji.  
   >   
   >  Najprostszym sposobem, aby rozwiązać ten problem dotyczy Zamknij wszystkie inne aplikacje języka JavaScript. W przeciwnym razie można otworzyć Menedżera zadań Windows, aby uruchomić aplikację i zanotuj identyfikatorów procesów wwahost.exe. Po określeniu proces do dołączenia w **dostępne procesy** okno dialogowe wwahost.exe aplikacji będzie mieć identyfikator, który jest inny niż te, które zostały zanotowane.  
  
5. Wybierz **dołączyć**.  
  
   Program Visual Studio dołącza debuger do procesu. Wykonywanie jest kontynuowane, dopóki punkt przerwania zostanie osiągnięty, ręcznie zawieszenie wykonywania, wystąpi nieobsługiwany wyjątek, lub kończy się w aplikacji.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie aplikacji w programie Visual Studio](../debugger/debug-store-apps-in-visual-studio.md)   