---
title: 'Przewodnik: Tworzenie środowiska kompilacji na wielu komputerach'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, building on multiple computers
- build environment, MSBuild
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2dc88c3861adb8b1d9f239d6ceedee2b76bc2e25
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49951616"
---
# <a name="walkthrough-create-a-multiple-computer-build-environment"></a>Przewodnik: Tworzenie środowiska kompilacji na wielu komputerach

Można utworzyć środowisko budowania w obrębie organizacji przez zainstalowanie programu Visual Studio na komputerze-hoście, a następnie kopiowanie różnych plików i ustawień na inny komputer, aby uczestniczyć w kompilacji. Nie trzeba zainstalować program Visual Studio na innym komputerze.

Ten dokument nie przyznaje praw do rozpowszechniania oprogramowania zewnętrznie lub dostarcza kompilacji środowiska stronom trzecim.

> Zrzeczenie odpowiedzialności<br /><br /> W tym dokumencie znajduje się na "jako — jest" podstawy. Podczas gdy przetestowaliśmy opisane kroki, nie możemy wyczerpująco przetestować każdej konfiguracji. Firma Microsoft będzie podejmować próby aktualność dokumentu o wszelkie dodatkowo uzyskane informacje. Informacje i poglądy wyrażone w tym dokumencie, w tym adresy URL i inne odnośniki do witryn internetowych, mogą ulec zmianie bez powiadomienia. Microsoft nie udziela żadnych gwarancji, wyraźnych ani dorozumianych, w związku z informacjami przedstawionymi tutaj. Użytkownik jest odpowiedzialny za jej pomocą.<br /><br /> W tym dokumencie nie umożliwiają żadnych praw do własności intelektualnej w jakimkolwiek produkcie firmy Microsoft. Można kopiować i używać tego dokumentu do wewnętrznych celów referencyjnych.<br /><br /> Użytkownik nie ma obowiązku przekazywania firmie Microsoft, masz jakieś sugestie, komentarze lub inne opinie ("opinia") odnoszących się do tego dokumentu. Jednakże wszystkie opinie dobrowolnie może służyć w Products firmy Microsoft i związanych z nimi specyfikacjach lub innej dokumentacji (zbiorczo "Offerings Microsoft"), który z kolei mogą opierać przez innych stronach trzecich do opracowywania własnych produktów. W związku z tym Jeśli nadasz Microsoft Feedback w dowolnej wersji systemu w tym dokumencie lub Offerings firmy Microsoft do których mają zastosowanie, wyrażasz zgodę: () firmy Microsoft mogą bez ograniczeń wykorzystywać, odtworzenie, licencji, dystrybucja i w przeciwnym razie komercjalizowania opinii użytkownika w dowolnym programie Microsoft Oferta; (b) należy również przyznać stron trzecich, bez opłaty, tylko tych praw patentowych niezbędne do obsługi innych produktów lub korzystać z określonymi częściami Product firmy Microsoft, które zawierają swoje opinie; i (c) użytkownik nie będzie przesyłał firmy Microsoft opinię (i), czy masz podejrzewać, podlega postanowieniom oświadczenia o prawach autorskich, patentów lub inne prawa własności intelektualnej ani po prawej stronie żadnym podmiotom trzecim; lub (ii) z zastrzeżeniem postanowień licencyjnych, które starają się wymagają żadnych Offering firmy Microsoft zawierająca lub pochodzące z takich opinii lub innych własności intelektualnej Microsoft licencji lub w inny sposób udostępniane osób trzecich.

Ten instruktaż został zweryfikowany w kontekście następujących systemów operacyjnych:

- Windows 8 (x86 i x64)
- Windows 7 Ultimate
- Windows Server 2008 R2 Standard

Po wykonaniu kroków w tym instruktażu, można użyć środowiska wielu komputerów do kompilowania tych rodzajów aplikacji:

- Aplikacje pulpitu C++, które używają Windows 8 SDK
- Visual Basic lub C# aplikacji komputerowych, których platformą docelową .NET Framework 4.5

Nie można użyć środowiska wielu komputerów do kompilowania tych rodzajów aplikacji:

- Aplikacje platformy uniwersalnej systemu Windows. Aby kompilować aplikacje platformy uniwersalnej systemu Windows, należy zainstalować program Visual Studio na komputerze kompilacji.
- Aplikacje klasyczne, przeznaczonych dla programu .NET Framework 4 lub wersji wcześniejszych. Do kompilowania tych rodzajów aplikacji, należy zainstalować na komputerze kompilacji programu Visual Studio lub zestawy referencyjne platformy .NET i narzędzi (z Windows 7.1 SDK).

## <a name="prerequisites"></a>Wymagania wstępne

- Program Visual Studio z **programowanie aplikacji klasycznych dla platformy .NET** zainstalowanym obciążeniem.

## <a name="install-software-on-the-computers"></a>Instalowanie oprogramowania na komputerach

Najpierw skonfigurować komputer hosta, a następnie skonfigurować komputer kompilacji.

Po zainstalowaniu programu Visual Studio na komputerze-hoście, Utwórz pliki i ustawienia, które będzie kopiować do komputera kompilacji później. Można zainstalować program Visual Studio na x86 lub x64 komputera, ale architektura komputera kompilacji musi odpowiadać architekturze komputera-hosta.

1. Na komputerze-hoście Zainstaluj program Visual Studio.

2. Na komputerze kompilacji Instalowanie programu .NET Framework 4.5 lub nowszej. Aby sprawdzić, czy jest zainstalowany, sprawdź, czy **wersji** wpis w podkluczu rejestru **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework setup\ndp\v4\full ma** ma wartość **4.5** lub nowszej.

## <a name="copy-files-from-the-host-computer-to-the-build-computer"></a>Kopiuj pliki z komputera hosta do komputera kompilacji

W tej sekcji omówiono kopiowania określonych plików, kompilatorów, narzędzi do kompilacji, aktywów programu MSBuild i ustawień rejestru z komputera hosta do komputera kompilacji. W poniższych instrukcjach przyjęto, że po zainstalowaniu programu Visual Studio w lokalizacji domyślnej na komputerze-hoście; Jeśli został zainstalowany w innej lokalizacji, należy odpowiednio dostosować czynności.

- Na x86 komputera, domyślna lokalizacja to *C:\Program Files\Microsoft Visual Studio 11.0*
- Na x64 komputera, domyślna lokalizacja to *C:\Program Files (x86) \Microsoft Visual Studio 11.0*

Należy zauważyć, że nazwa *Program Files* folderu jest zależna od systemu operacyjnego, który jest zainstalowany. Na x86 komputera, nazwa jest *Program Files*; x64 komputera, nazwa jest *Program Files (x86)*. Niezależnie od architektury systemu, ten instruktażu odwołuje się do *Program Files* folder jako *% ProgramFiles %*.

> [!NOTE]
> Na komputerze kompilacji wszystkie odpowiednie pliki muszą być na tym samym dysku; litera dysku może być jednak różni się od litery dysku dla dysku, na którym zainstalowano program Visual Studio na komputerze-hoście. W każdym przypadku konieczne jest uwzględnienie lokalizacji plików podczas tworzenia wpisów rejestru zgodnie z opisem w dalszej części tego dokumentu.

### <a name="copy-the-windows-sdk-files-to-the-build-computer"></a>Skopiuj pliki Windows SDK do komputera kompilacji

1. Jeśli masz tylko Windows SDK dla systemu Windows 8 zainstalowane, skopiuj te foldery rekurencyjnie z komputera hosta do komputera kompilacji:

   - %ProgramFiles%\Windows Kits\8.0\bin\

   - %ProgramFiles%\Windows Kits\8.0\Catalogs\

   - %ProgramFiles%\Windows Kits\8.0\DesignTime\

   - %ProgramFiles%\Windows Kits\8.0\include\

   - %ProgramFiles%\Windows Kits\8.0\Lib\

   - %ProgramFiles%\Windows Kits\8.0\Redist\

   - %ProgramFiles%\Windows Kits\8.0\References\

     Jeśli posiadasz również inne zestawy Windows 8...

   - Program Microsoft Windows Assessment and Deployment Kit

   - Zestaw Microsoft Windows Driver Kit

   - Zestaw certyfikacji sprzętu Microsoft Windows

     .. .mogli zainstalować pliki do *%ProgramFiles%\Windows Kits\8.0* folderów, które są wymienione w poprzednim kroku, a ich postanowień licencyjnych może nie pozwalać na praw serwera kompilacji dla tych plików. Sprawdź warunki licencji dla każdego zainstalowanego zestawu Windows sprawdzić, czy pliki mogą być kopiowane do komputera kompilacji. Jeśli postanowienia licencyjne nie dopuszczają praw serwera kompilacji, Usuń pliki z komputera kompilacji.

2. Kopiuj następujące foldery rekurencyjnie z komputera hosta do komputera kompilacji:

    - %ProgramFiles%\Microsoft SDKs\Windows\v8.0A\bin\NETFX 4.0 Tools\

    - %ProgramFiles%\Common Files\Merge Modules\

    - %ProgramFiles%\Microsoft Visual Studio 11.0\VC\

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\Tools\ProjectComponents\

    - %ProgramFiles%\MSBuild\Microsoft.Cpp\v4.0\V110\

    - %ProgramFiles%\Reference Assemblies\Microsoft\Framework\\. NETCore\v4.5\

    - %ProgramFiles%\Reference Assemblies\Microsoft\Framework\\. NETFramework\v4.5\

3. Skopiuj następujące pliki z komputera hosta do komputera kompilacji:

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\msobj110.dll

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\mspdb110.dll

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\mspdbcore.dll

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\mspdbsrv.exe

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\msvcdis110.dll

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\Tools\makehm.exe

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\Tools\VCVarsQueryRegistry.bat

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\Tools\vsvars32.bat

4. Następujące biblioteki środowiska uruchomieniowego Visual C++ są wymagane tylko wtedy, gdy uruchomienia kompilacji wyjść na komputerze kompilacji — na przykład w ramach automatycznego testowania. Pliki zwykle znajdują się w podfolderach *%ProgramFiles%\Microsoft Visual Studio 11.0\VC\redist\x86* lub *%ProgramFiles%\Microsoft Visual Studio 11.0\VC\redist\x64* folderu w zależności od architektury systemu. Na x86 systemów, skopiuj x86 pliki binarne do *Windows\System32* folderu. Na x64 systemów, skopiuj x86 pliki binarne do *Windows\SysWOW64* folder i x64 dane binarne do *Windows\System32* folderu.

    - \Microsoft.VC110.ATL\atl110.dll

    - \Microsoft.VC110.CRT\msvcp110.dll

    - \Microsoft.VC110.CRT\msvcr110.dll

    - \Microsoft.VC110.CXXAMP\vcamp110.dll

    - \Microsoft.VC110.MFC\mfc110.dll

    - \Microsoft.VC110.MFC\mfc110u.dll

    - \Microsoft.VC110.MFC\mfcm110.dll

    - \Microsoft.VC110.MFC\mfcm110u.dll

    - \Microsoft.VC110.MFCLOC\mfc110chs.dll

    - \Microsoft.VC110.MFCLOC\mfc110cht.dll

    - \Microsoft.VC110.MFCLOC\mfc110deu.dll

    - \Microsoft.VC110.MFCLOC\mfc110enu.dll

    - \Microsoft.VC110.MFCLOC\mfc110esn.dll

    - \Microsoft.VC110.MFCLOC\mfc110fra.dll

    - \Microsoft.VC110.MFCLOC\mfc110ita.dll

    - \Microsoft.VC110.MFCLOC\mfc110jpn.dll

    - \Microsoft.VC110.MFCLOC\mfc110kor.dll

    - \Microsoft.VC110.MFCLOC\mfc110rus.dll

    - \Microsoft.VC110.OPENMP\vcomp110.dll

5. Skopiuj następujące pliki z *Debug_NonRedist\x86* lub *Debug_NonRedist\x64* folderu na komputerze kompilacji, zgodnie z opisem w [przygotowanie maszyny testowej do uruchomienia debugowania pliku wykonywalnego](/cpp/ide/preparing-a-test-machine-to-run-a-debug-executable). Żadne inne pliki nie mogą być kopiowane.

    - \Microsoft.VC110.DebugCRT\msvcp110d.dll

    - \Microsoft.VC110.DebugCRT\msvcr110d.dll

    - \Microsoft.VC110.DebugCXXAMP\vcamp110d.dll

    - \Microsoft.VC110.DebugMFC\mfc110d.dll

    - \Microsoft.VC110.DebugMFC\mfc110ud.dll

    - \Microsoft.VC110.DebugMFC\mfcm110d.dll

    - \Microsoft.VC110.DebugMFC\mfcm110ud.dll

    - \Microsoft.VC110.DebugOpenMP\vcomp110d.dll

## <a name="create-registry-settings"></a>Tworzenie ustawień rejestru

Musisz utworzyć wpisy rejestru, aby skonfigurować ustawienia dla programu MSBuild.

1. Określ folder nadrzędny do wpisów rejestru. Wszystkie wpisy rejestru są tworzone w ramach tego samego klucza nadrzędnego. Na x86 komputera, klucz nadrzędny to **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft**. Na x64 komputer klucza nadrzędnego jest **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft**. Niezależnie od architektury systemu ten instruktażu odwołuje się do klucza nadrzędnego jako % RegistryRoot %.

    > [!NOTE]
    > Jeśli architektura komputera hosta różni się od architektury komputera kompilacji, upewnij się, że używasz właściwego klucza nadrzędnego na każdym komputerze. Jest to szczególnie ważne, jeśli automatyzujesz proces eksportowania.
    >
    > Jeśli używasz innej litery dysku na komputerze kompilacji niż ten, którego używasz na komputerze-hoście, upewnij się również zmienić wartości wpisów rejestru w celu dopasowania.

2. Utwórz następujące wpisy rejestru na komputerze kompilacji. Wszystkie te pozycje są ciągami (typ == "REG_SZ" w rejestrze). Ustaw wartości tych wpisów tak samo jako wartości porównywalnych wpisów na komputerze-hoście.

   - **% RegistryRoot %\\. NETFramework\v4.0.30319\AssemblyFoldersEx\VCMSBuild Assemblies@(Default) publiczne**

   - <strong>%RegistryRoot%\Microsoft SDKs\Windows\v8.0@InstallationFolder</strong>

   - <strong>%RegistryRoot%\Microsoft SDKs\Windows\v8.0A@InstallationFolder</strong>

   - <strong>%RegistryRoot%\Microsoft SDKs\Windows\v8.0A\WinSDK-NetFx40Tools@InstallationFolder</strong>

   - <strong>%RegistryRoot%\Microsoft SDKs\Windows\v8.0A\WinSDK-NetFx40Tools-x86@InstallationFolder</strong>

   - **% RegistryRoot %\VisualStudio\11.0@Source katalogów**

   - <strong>% RegistryRoot %\VisualStudio\11.0\Setup\VC@ProductDir</strong>

   - <strong>% RegistryRoot %\VisualStudio\SxS\VC7@FrameworkDir32</strong>

   - <strong>% RegistryRoot %\VisualStudio\SxS\VC7@FrameworkDir64</strong>

   - <strong>% RegistryRoot %\VisualStudio\SxS\VC7@FrameworkVer32</strong>

   - <strong>% RegistryRoot %\VisualStudio\SxS\VC7@FrameworkVer64</strong>

   - **% RegistryRoot %\VisualStudio\SxS\VC7@11.0**

   - **% RegistryRoot %\VisualStudio\SxS\VS7@11.0**

   - <strong>%RegistryRoot%\Windows Kits\Installed Roots@KitsRoot</strong>

   - <strong>% RegistryRoot %\MSBuild\ToolsVersions\4.0\11.0@VCTargetsPath</strong>

   - <strong>% RegistryRoot %\MSBuild\ToolsVersions\4.0\11.0@VCTargetsPath10</strong>

   - <strong>% RegistryRoot %\MSBuild\ToolsVersions\4.0\11.0@VCTargetsPath11</strong>

   X64 komputer kompilacji, również Utwórz następujący wpis rejestru i odnoszą się do komputera hosta, aby określić sposób ustawienia go.

   - <strong>%RegistryRoot%\Microsoft SDKs\Windows\v8.0A\WinSDK-NetFx40Tools-x64@InstallationFolder</strong>

   Jeśli komputer kompilacji posiada x64 i chcesz użyć 64-bitowej wersji programu MSBuild lub jeśli używasz usługi kompilacji Team Foundation Server na x64 komputerów, utwórz następujące wpisy rejestru w natywnych 64-bitowego rejestru. Zapoznaj się z komputera hosta, aby uzyskać informacje o ustawianiu tych wpisów.

   - <strong>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\11.0\Setup\VS@ProductDir</strong>

   - <strong>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSBuild\ToolsVersions\4.0\11.0@VCTargetsPath</strong>

   - <strong>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSBuild\ToolsVersions\4.0\11.0@VCTargetsPath10</strong>

   - <strong>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSBuild\ToolsVersions\4.0\11.0@VCTargetsPath11</strong>

## <a name="set-environment-variables-on-the-build-computer"></a>Ustawianie zmiennych środowiskowych na komputerze kompilacji

Aby użyć programu MSBuild na komputerze kompilacji, należy ustawić zmienne środowiskowe ścieżki. Możesz użyć *vcvarsall.bat* do ustawiania zmiennych, lub ręcznie skonfigurować je.

### <a name="use-vcvarsallbat-to-set-environment-variables"></a>Vcvarsall.bat umożliwia ustawianie zmiennych środowiskowych

Otwórz **polecenia** okno na komputerze kompilacji i uruchomienia *% Program Files%\Microsoft Visual Studio 11.0\VC\vcvarsall.bat*. Argument wiersza polecenia można użyć do określenia zestawu narzędzi, której chcesz użyć — x86, natywne x64 lub x64 kompilator krzyżowy. Jeśli nie zostanie określony argument wiersza polecenia x86 używany jest zestaw narzędzi.

W tej tabeli opisano obsługiwane argumenty dla *vcvarsall.bat*:

|Vcvarsall.bat argument|Kompilator|Architektura komputera kompilacji.|Architektura obiektów wyjściowych kompilacji|
| - |--------------| - | - |
|x86 (ustawienie domyślne)|Natywne 32-bitowe|x86, x64|x86|
|x86_amd64|x64 cross|x86, x64|X64|
|amd64|x64 natywne|X64|X64|

Jeśli *vcvarsall.bat* zostanie uruchomiony pomyślnie — to znaczy bez komunikatu o błędzie jest wyświetlany — można pominąć następny krok i kontynuować [instalowanie zestawów programu MSBuild do globalnej pamięci podręcznej zestawów (GAC) na komputerze kompilacji](../ide/walkthrough-creating-a-multiple-computer-build-environment.md#InstallingMSBuildToGAC)części tego dokumentu.

### <a name="manually-set-environment-variables"></a>Ręczne ustawianie zmiennych środowiskowych

1. Aby ręcznie skonfigurować środowisko wiersza polecenia, Dodaj tę ścieżkę do zmiennej środowiskowej PATH:

    - %Program Files%\Microsoft Visual Studio 11.0\Common7\IDE

2. Opcjonalnie można również dodać następujące ścieżki do zmiennej PATH, aby ułatwić tworzenie rozwiązania za pomocą programu MSBuild.

   Za pomocą natywnego programu 32-bitowy MSBuild, należy dodać te ścieżki do zmiennej PATH:

   - %Program Files%\Microsoft SDKs\Windows\v8.0A\bin\NETFX 4.0 Tools

   - %windir%\Microsoft.NET\Framework\v4.0.30319

   Jeśli chcesz użyć natywnych 64-bitowy MSBuild, należy dodać te ścieżki do zmiennej PATH:

   - %Program Files%\Microsoft SDKs\Windows\v8.0A\bin\NETFX 4.0 Tools\x64

   - %windir%\Microsoft.NET\Framework64\v4.0.30319

## <a name="install-msbuild-assemblies-to-the-global-assembly-cache-gac-on-the-build-computer"></a>Instalowanie zestawów programu MSBuild do globalnej pamięci podręcznej zestawów (GAC) na komputerze kompilacji

Program MSBuild wymaga kilku dodatkowych zestawów do zainstalowania GAC na komputerze kompilacji.

1. Kopiuj następujące zestawy z komputera hosta do komputera kompilacji. Ponieważ zostaną one zainstalowane w GAC, nie ma znaczenia, gdzie umieścić na komputerze kompilacji.

    - %ProgramFiles%\MSBuild\Microsoft.Cpp\v4.0\v110\Microsoft.Build.CPPTasks.Common.v110.dll

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\CommonExtensions\Microsoft\VC\Project\Microsoft.VisualStudio.Project.VisualC.VCProjectEngine.dll

    - %ProgramFiles%\Microsoft Visual Studio 11.0\Common7\IDE\PublicAssemblies\Microsoft.VisualStudio.VCProjectEngine.dll

2. Aby zainstalować zestawy GAC, zlokalizuj *gacutil.exe* na komputerze kompilacji — zwykle jest w %ProgramFiles%\Microsoft SDKs\Windows\v8.0A\bin\NETFX 4.0 narzędzia\\. Jeśli nie możesz znaleźć tego folderu, powtórz kroki opisane w [skopiuj pliki z komputera hosta do komputera kompilacji](../ide/walkthrough-creating-a-multiple-computer-build-environment.md#CopyingFiles) sekcji tego przewodnika.

     Otwórz **polecenia** okno, które ma prawa administracyjne i uruchom następujące polecenie dla każdego pliku:

     **gacutil -i \<pliku >**

    > [!NOTE]
    > Ponowne uruchomienie komputera może być wymagane dla zestawu w pełni zainstalować w GAC.

## <a name="build-projects"></a>Kompilowanie projektów

Potoki usługi Azure można użyć do tworzenia projektów programu Visual Studio i rozwiązania lub tworzyć je w wierszu polecenia. Korzystając z potoków usługi Azure do tworzenia projektów, wywołuje MSBuild pliku wykonywalnego, który odpowiada architekturze systemu. W wierszu polecenia można użyć 32-bitowej platformy MSBuild lub 64-bitowej platformy MSBuild i można wybrać architekturę programu MSBuild przez ustawienie zmiennej środowiskowej PATH lub bezpośrednie wywołanie pliku wykonywalnego architektury programu MSBuild.

Aby użyć *msbuild.exe* w wierszu polecenia Uruchom następujące polecenie, w którym *przy* jest symbolem zastępczym dla nazwy rozwiązania.

**msbuild** *solution.sln*

Aby uzyskać więcej informacji na temat sposobu użycia MSBuild w wierszu polecenia, zobacz [wiersza polecenia](../msbuild/msbuild-command-line-reference.md).

## <a name="create-the-build-environment-so-that-it-can-be-checked-into-source-control"></a>Tworzenie środowiska kompilacji, dzięki czemu mogą być sprawdzone w formancie źródła

Można utworzyć środowisko budowania, które mogą być rozmieszczone na różnych komputerach i nie wymaga "GAC"-ing plików lub modyfikowania ustawień rejestru. Następujące kroki są tylko jeden ze sposobów osiągnięcia tego. Dostosuj te procedury do unikalnych cech środowiska kompilacji.

> [!NOTE]
> Należy wyłączyć przyrostowe kompilowanie, aby *tracker.exe* nie będzie sygnalizować błąd, podczas kompilacji. Aby wyłączyć przyrostowe kompilowanie, ustaw ten parametr kompilacji:
>
> **msbuild** *solution.sln* **/p:TrackFileAccess=false**

1. Tworzenie *Depot* katalogu na komputerze-hoście.

     Te kroki odnoszą się do katalogu jako Depot %.

2. Skopiuj pliki i katalogi zgodnie z opisem w [skopiuj pliki z komputera hosta do komputera kompilacji](../ide/walkthrough-creating-a-multiple-computer-build-environment.md#CopyingFiles) sekcji tego przewodnika, z wyjątkiem wklej je w obszarze *% Depot %* katalogu, który został właśnie utworzony. Na przykład skopiuj z *%ProgramFiles%\Windows Kits\8.0\bin* do *%Depot%\Windows Kits\8.0\bin*.

3. Kiedy pliki są wklejane w *% Depot %*, wprowadź następujące zmiany:

    - W % Depot%\MSBuild\Microsoft.Cpp\v4.0\v110\Microsoft.CPP.Targets \Microsoft.Cpp.InvalidPlatforms.targets\\, \Microsoft.cppbuild.targets\\i \Microsoft.CppCommon.targets\\, zmienić każde wystąpienie z

         AssemblyName="Microsoft.Build.CppTasks.Common.v110, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"

         na

         AssemblyFile="$(VCTargetsPath11)Microsoft.Build.CppTasks.Common.v110.dll".

         Nazewnictwo opiera się na opierało.

    - W % Depot % \MSBuild\Microsoft.Cpp\v4.0\v110\Microsoft.CPPClean.Targets należy zmienić każde wystąpienie

         AssemblyName="Microsoft.Build.CppTasks.Common.v110, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"

         na

         AssemblyFile="$(VCTargetsPath11)Microsoft.Build.CppTasks.Common.v110.dll".

4. Tworzenie *.props* pliku — na przykład *Partner.AutoImports.props*— i umieść go w katalogu głównym folderu, który zawiera projekty. Ten plik jest używany do ustawiania zmiennych, które są używane przez program MSBuild do znajdowania poszczególnych zasobów. Jeśli zmienne nie są ustawiane przez ten plik, są one ustalane przez inne *.props* plików i *.targets* pliki, które opierają się na wartości rejestru. Ponieważ nie ustawiamy żadnych wartości rejestru, te zmienne będą puste, a kompilacja zakończy się niepowodzeniem. Zamiast tego dodać ten element, aby *Partner.AutoImports.props*:

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <!-- This file must be imported by all project files at the top of the project file. -->
    <Project ToolsVersion="4.0"
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <PropertyGroup>
    <VCTargetsPath>$(DepotRoot)MSBuild\Microsoft.Cpp\v4.0\v110\</VCTargetsPath>
    <VCTargetsPath11>$(DepotRoot)MSBuild\Microsoft.Cpp\v4.0\v110\</VCTargetsPath11>
    <MSBuildExtensionsPath>$(DepotRoot)MSBuild</MSBuildExtensionsPath>
    <MSBuildExtensionsPath32>$(DepotRoot)MSBuild</MSBuildExtensionsPath32>
    <VCInstallDir_110>$(DepotRoot)Microsoft Visual Studio 11.0\VC\</VCInstallDir_110>
    <VCInstallDir>$(VCInstallDir_110)</VCInstallDir>
    <WindowsKitRoot>$(DepotRoot)Windows Kits\</WindowsKitRoot>
    <WindowsSDK80Path>$(WindowsKitRoot)</WindowsSDK80Path>
    <WindowsSdkDir_80>$(WindowsKitRoot)8.0\</WindowsSdkDir_80>
    <WindowsSdkDir>$(WindowsSDKDir_80)</WindowsSdkDir>
    <WindowsSdkDir_80A>$(DepotRoot)Microsoft SDKs\Windows\v8.0A\</WindowsSdkDir_80A>
    </PropertyGroup>
    </Project>
    ```

5. W każdym z plików projektu, Dodaj następujący wiersz u góry, po `<Project Default Targets...>` wiersza.

    ```xml
    <Import Project="$([MSBuild]::GetDirectoryNameOfFileAbove($(MSBuildThisFileDirectory), Partner.AutoImports.props))\Partner.AutoImports.props"/>
    ```

6. Zmień środowisko wiersza polecenia w następujący sposób:

    - Ustaw magazyn =*lokalizację katalogu magazynu, który został utworzony w kroku 1*

    - Ustaw ścieżkę = % path %; *lokalizacji programu MSBuild na komputerze*; %D epot%\Windows\System32;%D epot%\Windows\SysWOW64;%D 15.0\Common7\IDE\ programu Visual Studio epot%\Microsoft

       Dla natywnej kompilacji 64-bitowej, wskaż 64-bitowy MSBuild.

## <a name="see-also"></a>Zobacz także

- [Przygotowanie maszyny testowej do uruchomienia debugowania pliku wykonywalnego](/cpp/ide/preparing-a-test-machine-to-run-a-debug-executable)
- [Informacje dotyczące wiersza polecenia](../msbuild/msbuild-command-line-reference.md)