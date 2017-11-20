---
title: "Visual Studio IDE omówienie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 10/03/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 772b6cf4-cee5-42d0-bc18-b4eb07e22ff0
caps.latest.revision: "35"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: ee41f513af60fc475616474d493e330d1289210d
ms.sourcegitcommit: fb751e41929f031d1a9247bc7c8727312539ad35
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2017
---
# <a name="visual-studio-ide-overview"></a>Visual Studio IDE — omówienie
Środowisko projektowe interaktywne programu Visual Studio (IDE) jest creative konsoli uruchamianie, który służy do wyświetlania i edytowania niemal wszystkich typów kodu i następnie debugowania, kompilacji i publikowanie aplikacji dla systemu Android, iOS, Windows, sieci web i chmury. Dostępne są wersje dla systemów Mac i systemu Windows. W tym temacie przedstawiono funkcje programu Visual Studio IDE. Omówimy kilka rzeczy, można z programu Visual Studio oraz jak zainstalować i korzystać z niego, tworzenie prostego projektu, uzyskać wskaźniki dotyczące debugowania i wdrażanie kodu i zapoznaj się z różnych okien narzędzi.  

## <a name="what-can-you-do-with-the-visual-studio-ide"></a>Co należy zrobić z programu Visual Studio IDE
Czy chcesz utworzyć aplikację dla telefonów z systemem Android? Możesz to zrobić. Jak utworzyć gier najnowocześniejszych za pomocą języka C++? Można to zrobić za i znacznie więcej. Program Visual Studio udostępnia szablony, które ułatwiają witryn sieci Web, gier, aplikacji klasycznych, aplikacje mobilne, aplikacje pakietu Office i więcej.  

![Projekty Visual Studio](../ide/media/VSIDE_Tour_Projects_List.png)

Lub, wystarczy otworzyć kodu uzyskać z niemal dowolnego miejsca i pobrać pracy. Zobacz Projekt w witrynie GitHub, który chcesz? Tylko sklonować repozytorium, otwórz go w programie Visual Studio i programować!  

### <a name="create-mobile-apps"></a>Tworzenie aplikacji mobilnych
Można utworzyć natywnej aplikacji mobilnych dla różnych platform, za pomocą Visual C# i Xamarin lub Visual C++ lub aplikacje hybrydowe z platformy Apache Cordova przy użyciu języka JavaScript. Można zapisywać przenośnych gry dla platformy Unity, niezr, DirectX i Cocos. Visual Studio zawiera emulatorze systemu Android, aby uruchomić i debugowania aplikacji systemu Android.  

Można skorzystać z możliwości chmury dla aplikacji mobilnych, tworząc usługi aplikacji Azure. Usługi aplikacji Azure Włączanie aplikacji do przechowywania danych w chmurze, bezpieczne uwierzytelnianie użytkowników i automatycznie skalować zasobów lub w dół do uwzględnienia na potrzeby aplikacji i firmy. Aby dowiedzieć się więcej, zobacz [tworzenia aplikacji mobilnych](https://www.visualstudio.com/vs/mobile-app-development/).  

### <a name="create-cloud-apps-for-azure"></a>Tworzenie aplikacji w chmurze na platformie Azure
Program Visual Studio oferuje zestaw narzędzi, które umożliwiają łatwe tworzenie aplikacji z obsługą chmury obsługiwane przez usługę Microsoft Azure. Można skonfigurować, tworzenia, debugowania pakietu i wdrożyć aplikacje i usługi Microsoft Azure bezpośrednio z IDE. Korzystaj z usług Azure dla aplikacji za pomocą usług połączonych. Aby uzyskać narzędzia Azure dla platformy .NET, wybierz **Azure programowanie** obciążenia podczas instalowania programu Visual Studio. Aby uzyskać więcej informacji, zobacz [Visual Studio Tools for Azure](https://www.visualstudio.com/vs/azure-tools/).  

### <a name="create-apps-for-the-web"></a>Tworzenie aplikacji dla sieci web
Nasze współczesnym świecie dyski sieci web i Visual Studio ułatwia pisanie aplikacji dla niego. Można utworzyć aplikacji sieci web ASP.NET, Node.js, Python, JavaScript i TypeScript. Visual Studio rozumie struktur sieci web, takich jak kątową, jQuery, Express i inne. Oprogramowanie .NET Core i ASP.NET Core uruchomienia w systemach operacyjnych Windows, Mac i Linux. Aby uzyskać więcej informacji, zobacz [nowoczesnych narzędzi sieci Web](https://www.visualstudio.com/vs/modern-web-tooling/).  

### <a name="write-code-in-a-world-class-editing-environment"></a>Pisanie kodu w klasie world środowisko edycji
Programu Visual Studio ułatwia pisanie kodu szybko i łatwo przy użyciu funkcji, takich jak kolorowanie składni, uzupełniania instrukcji, IntelliSense (podręczny opis elementu zaznaczonego kodu), kodu zwijania, ustawianie punktów przerwania dla debugowania i o wiele więcej.  

![Przykład kodu JavaScript](../ide/media/vside_tour_javascript_example.gif)

Aby dowiedzieć się więcej, zobacz [pisanie kodu w edytorze kodu i tekstu](https://docs.microsoft.com/visualstudio/ide/writing-code-in-the-code-and-text-editor).  

Visual Studio można wykonać wykonywanie wielu czynności więcej pomocy. Aby uzyskać bardziej szczegółowy wykaz, zobacz [programu Visual Studio IDE](https://www.visualstudio.com/vs/).  

## <a name="install-the-visual-studio-ide"></a>Zainstaluj program Visual Studio IDE
Aby rozpocząć pracę, Pobierz program Visual Studio i zainstaluj go w systemie. Możesz pobrać go w [programu Visual Studio 2017](https://www.visualstudio.com/vs/visual-studio-2017/).  

Program Visual Studio jest teraz bardziej lekkie niż kiedykolwiek! Nowe Instalator moduły umożliwia wybierz i zainstaluj *obciążeń*, które są grup funkcji potrzebnych do programowania języka lub platformy wolisz. Ta strategia pomaga w zapewnieniu rozmiaru instalacji programu Visual Studio mniejszy niż kiedykolwiek wcześniej, co oznacza instalowany i aktualizuje szybciej zbyt.  

![Instalator programu Visual Studio](../ide/media/vside_tour_install_dialog.png)

Oprócz instalacji lepszą wydajność Visual Studio 2017 ma również krótszą rozruchu IDE i załadować czasy rozwiązania.

Aby dowiedzieć się więcej o konfigurowaniu programu Visual Studio w systemie, zobacz [zainstalować program Visual Studio 2017](https://docs.microsoft.com/visualstudio/install/install-visual-studio).  

## <a name="sign-in"></a>Rejestrowanie
Po uruchomieniu programu Visual Studio po raz pierwszy, można opcjonalnie Zaloguj się przy użyciu konta Microsoft lub pracy lub konta służbowego. Trwa logowanie, umożliwia synchronizowanie ustawień programu Visual Studio, takich jak układów okien na wielu urządzeniach. On również łączy automatycznie usługi, które może być konieczne, takie jak subskrypcje platformy Azure i Visual Studio Team Services.  

## <a name="create-a-program"></a>Utwórz program
Dobrym sposobem Dowiedz się więcej o coś jest jej używać! Załóżmy zajrzyj dostęp i utworzyć nowe, proste program.  

1. Otwórz program Visual Studio. W menu, wybierz **pliku**, **nowy**, **projektu**.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_NewProject1.png)

  Alternatywnie można utworzyć nowy projekt za pomocą strony początkowej. Aby uzyskać więcej informacji, zobacz [korzystają z możliwości przeprojektowana strona początkowa (blog)](https://blogs.msdn.microsoft.com/visualstudio/2016/11/29/harness-the-power-of-the-redesigned-start-page/).  

1. **Nowy projekt** okno dialogowe zawiera kilka szablonów projektu. Wybierz **uniwersalnych systemu Windows** kategorię w obszarze **Visual C#**, wybierz **pusta aplikacja (uniwersalna systemu Windows)** szablonu, a następnie wybierz pozycję **OK**przycisku.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_NewProject2.png)

  Spowoduje to utworzenie nowego projektu aplikacji puste uniwersalnych systemu Windows za pomocą Visual C# i XAML jako języków programowania. Zaczekaj, aż do bit Visual Studio skonfigurowanie projektu dla Ciebie. Jeśli zostanie wyświetlony monit o podanie informacji, po prostu zaakceptuj wartości domyślne teraz.  

1. W **nowe uniwersalnych projektów systemu Windows** okna dialogowego Zaakceptuj ustawienia domyślne, wybierając **OK**.  

1. Wkrótce powinien zostać wyświetlony ekran podobny do następującego zrzutu ekranu. Pliki projektu są wyświetlane po prawej stronie w okno Eksploratora rozwiązań.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_NewProject3.png)

1. W Eksploratorze rozwiązań wybierz małego czarny trójkąt obok pliku MainPage.xaml, aby go rozwinąć i powinna zostać wyświetlona pliku MainPage.xaml.cs poniżej. Wybierz ten plik (zawierający kod w języku C#) aby go otworzyć.  

  Kod C# MainPage.xaml.cs zostanie wyświetlony w edytorze kodu po lewej stronie ekranu. Zwróć uwagę, że składnia kodu jest automatycznie pokolorowane wskazująca różnych typów kodu, na przykład instrukcji lub komentarzy. Ponadto małych, pionowych linii kreskowanej w kodzie określają, które nawiasów klamrowych siebie, a później zlokalizować kod pomocy numery wierszy. Można wybrać znaków minus małe, opakowany można zwijać i rozwijać kodu. Ten kod zwijania funkcji umożliwia ukrywanie kodu, który nie jest konieczne, pomagając zminimalizować bałaganu na ekranie.  

  ![](../ide/media/VSIDE_Tour_NewProject3a.png)

  Brak dostępnych innych menu i okien narzędzi, ale Przyjrzyjmy teraz.  

1. Dodawanie przycisku do XAML, aby umożliwić użytkownikom możliwość interakcji z aplikacją. Aby to zrobić, otwórz plik MainPage.xaml. Widok podzielony pokazuje: projektanta powyżej, wizualnie objęcia formantów, a widok kodu poniżej, przedstawiający kodzie projektanta XAML. Po uruchomieniu program później, zobacz w Projektancie staje się oknem, które użytkownicy zobaczą, "form", i określa podstawowe języka XAML wyświetlaną w formularzu.  

1. W lewej części ekranu wybierz **przybornika** kartę, aby otworzyć przybornika. Przybornik zawiera szereg visual formanty, które można dodać do formularzy. Teraz po prostu dodamy kontrolkę przycisku.  

1. Rozwiń węzeł **formanty standardowe XAML** sekcji, a następnie przeciągnij formantu przycisku się do formularza do góry. (Dokładnej lokalizacji nie ma znaczenia).  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_Toolbox.png)

  Gdy wszystko będzie gotowe, powinny zostać wyświetlone informacje podobne do następującego.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_XAMLButton.png)

  Przycisk znajduje się w projektancie, a jego kod źródłowy (wyróżniony) jest automatycznie dodawany do projektanta XAML kodu.  

1. Teraz Zmień kod XAML. Zmień nazwę tekst w kodzie przycisk z `Button` do `Hello!`.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_XAMLButton2.png)

1. Teraz uruchomić aplikację. Można to zrobić, wybierając **Start** (![przycisk Start](../ide/media/VSIDE_StartButton.png)) przycisk na pasku narzędzi lub wybierając **F5** klucza, lub w menu, wybierając pozycję **debugowania**, **Rozpocznij debugowanie**.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_RunButton.png)

  Aplikacja rozpoczyna się procesu kompilacji i komunikaty o stanie są wyświetlane w oknie danych wyjściowych. Wkrótce powinien zostać wyświetlony formularz wyświetlane ze przycisk w nim. Masz teraz uruchomionej aplikacji.  

  ![Zrzut ekranu](../ide/media/VSIDE_Tour_RunProject.png)

  Oczywiście nie znacznie od razu, ale możesz dodać więcej funkcji do niego później, jeśli chcesz.  

1. Po zakończeniu uruchamiania programu, wybierz polecenie Zatrzymaj (![Zatrzymaj przycisku](../ide/media/VSIDE_StopButton.png)) przycisk na pasku narzędzi, zatrzymaj ją.

Załóżmy recap wykonanej do tej pory została: utworzyć nowy projekt C# uniwersalnych systemu Windows w programie Visual Studio, wyświetlić jego kod, dodać formantu do projektanta, zmienić kodu XAML i został uruchomiony projektu. Chociaż proces została uproszczona w tym przykładzie, to przedstawiono niektóre typowe części programu Visual Studio IDE, która będzie używana podczas opracowywania własnych aplikacji. Dalsze szczegóły tego przykładu, zobacz [tworzenie "Hello, world" app (XAML)](https://docs.microsoft.com/windows/uwp/get-started/create-a-hello-world-app-xaml-universal).  

## <a name="debug-test-and-improve-your-code"></a>Debugowanie, testowanie i poprawić kod
Nic nie uruchamia doskonale cały czas. Podczas pisania kodu, należy ją uruchomić i przetestować go do błędów i wydajności. Visual Studio najnowocześniejszych debugowania systemu umożliwia debugowania kodu uruchamianego w środowisku lokalnym projektu, urządzenie zdalne lub emulator, takich jak te dla urządzeń z systemem Android lub Windows Phone. Możesz kroków opisanych w jedną instrukcję kodu w czasie i sprawdzić zmiennych, możesz przejść, można przejrzeć aplikacji wielowątkowych i można ustawić punktów przerwania, które są osiągane tylko, gdy określony warunek jest spełniony. Można monitorować wartości zmiennych jako uruchamia kod i inne. Wszystkie te można zarządzać w edytorze kodu, dzięki czemu nie trzeba pozostaw kodu.  

![Debugowanie](../ide/media/VSIDE_Tour_Debugging.png)

Do testowania, programu Visual Studio oferuje testowania IntelliTest, obciążenia i testowanie wydajności i innych jednostek. Aby uzyskać więcej informacji na temat programu Visual Studio debugowanie procesu, zobacz [samouczek funkcji debugera](../debugger/debugger-feature-tour.md). Aby dowiedzieć się więcej na temat testowania, zobacz [narzędzi do testowania](https://www.visualstudio.com/vs/testing-tools/). Aby dowiedzieć się więcej na temat zwiększania wydajności aplikacji, zobacz [profilowania samouczek funkcji](../profiling/profiling-feature-tour.md).  

## <a name="deploy-your-finished-application"></a>Wdrażanie aplikacji Zakończono  
Gdy aplikacja jest gotowa do wdrożenia użytkownicy lub klienci, Visual Studio zawiera narzędzia w tym, czy w witrynie programu SharePoint lub technologii InstallShield lub Instalator Windows jest wdrażany Microsoft Store. Jest on wszystkie dostępne za pośrednictwem IDE. Aby uzyskać więcej informacji, zobacz [wdrażanie aplikacji, usług i składników](../deployment/deploying-applications-services-and-components.md).  

## <a name="quick-tour-of-the-ide"></a>Krótki przewodnik IDE
Aby dać visual Omówienie programu Visual Studio, na poniższej ilustracji przedstawiono Visual Studio z otwartego projektu oraz kilka okien narzędzi kluczy, które najprawdopodobniej będą używane:  

 - [Eksplorator rozwiązań](../ide/solutions-and-projects-in-visual-studio.md) umożliwia przeglądanie, przejdź i zarządzanie plikami kodu. Eksplorator rozwiązań może pomóc uporządkowanie kodu przez grupowanie plików do rozwiązania i projekty.  

 - [Edytor](../ide/writing-code-in-the-code-and-text-editor.md) okna, w którym będzie prawdopodobnie spędzają większość czasu, zawiera kod i umożliwia edytowanie kodu źródłowego i projektu interfejsu użytkownika.  

 - [Dane wyjściowe](../ide/reference/output-window.md) okno jest, gdzie Visual Studio wysyła jej powiadomień, takie jak debugowanie i komunikaty o błędach, ostrzeżenia kompilatora, publikowania komunikatów o stanie i. Każde źródło komunikatu ma własną kartę.  

 - [Team Explorer](https://www.visualstudio.com/docs/connect/work-team-explorer) umożliwia śledzenie elementów roboczych i udostępnianie kodu z innymi użytkownikami przy użyciu technologii kontroli wersji, takich jak [Git](https://git-scm.com/) i [Team Foundation wersji formantu (TFVC)] (https://www.visualstudio.com/docs/tfvc/overview) .  

 - [Cloud Explorer](/azure/vs-azure-tools-resources-managing-with-cloud-explorer) umożliwia wyświetlanie i zarządzania zasobami platformy Azure, takich jak maszyny wirtualne, tabel, baz danych i inne. Jeśli określonej operacji wymaga portalu Azure, Eksplorator chmury linki prowadzące do miejsca, w portalu Azure, które muszą przejść.  

![Visual Studio IDE](../ide/media/visualstudioide.png)  

Poniżej przedstawiono niektóre inne typowe funkcje wydajności w programie Visual Studio:  

- [Szybkie uruchamianie](https://docs.microsoft.com/en-us/visualstudio/ide/reference/quick-launch-environment-options-dialog-box) pole wyszukiwania jest to dobry sposób na szybkie wyszukiwanie informacji w programie Visual Studio. Rozpocząć wpisywanie nazwy niezależnie od, którego szukasz, i Visual Studio listy wyników przyjmujących dokładnie której ma nastąpić przejście. Szybkie uruchamianie zawiera również linki, który uruchamia Instalator programu Visual Studio dla wszystkich obciążeń lub poszczególnych składników.

  ![Pole wyszukiwania w usłudze szybkiego uruchamiania](../ide/media/VSIDE_Tour_QuickLaunch.png)

-  [Refaktoryzacja](../ide/refactoring-in-visual-studio.md) obejmuje operacje, takie jak inteligentnego zmiana nazwy zmiennych, przenoszenie wybrane wiersze kodu do oddzielnych funkcji przenoszenia kodu do innych lokalizacji, opcję parametrów funkcji i inne.  

 ![Refaktoryzacja](../ide/media/VSIDE_refactor.png)  

-  **IntelliSense** jest ogólny termin zbiór popularnych funkcji wyświetlania informacji o typie o kodzie bezpośrednio w edytorze i, w niektórych przypadkach można zapisać małe fragmenty kodu. Przypomina o dokumentacji podstawowej wbudowany w edytorze, co pozwala uniknąć konieczności wyszukiwania informacji o typie w oknie Pomoc. Funkcje IntelliSense zależy od języka. Aby uzyskać więcej informacji, zobacz [Visual C# IntelliSense](../ide/visual-csharp-intellisense.md), [Intellisense dla programu Visual C++](../ide/visual-cpp-intellisense.md), [IntelliSense dla JavaScript](../ide/javascript-intellisense.md), i [specyficzne dla języka Visual Basic IntelliSense](../ide/visual-basic-specific-intellisense.md). Na poniższej ilustracji przedstawiono niektóre funkcje IntelliSense w miejscu pracy:  

  ![Lista elementów członkowskich programu Visual Studio](../ide/media/vs2017_Intellisense.png)  

-  **Zygzaki** są faliste podkreślenie czerwony, które generują alerty błędów lub potencjalnych problemów w kodzie w czasie rzeczywistym w trakcie pisania. Dzięki temu można rozwiązać je natychmiast bez oczekiwania na błąd mają być wykryte podczas kompilacji lub czasu wykonywania. Jeśli Aktywuj wężyk, pojawi się dodatkowe informacje o tym błędzie. Żarówka może również zostać wyświetlony na lewym marginesie z sugestie dotyczące sposobu Napraw błąd. Aby uzyskać więcej informacji, zobacz [szybkie wykonywanie akcji dzięki żarówkom](../ide/perform-quick-actions-with-light-bulbs.md).  

 ![Zygzaki](../ide/media/vs2017_squiggle.png)  

-  [Hierarchii wywołań](../ide/reference/call-hierarchy.md) można otworzyć okna w menu kontekstowym edytora tekstu do wyświetlenia wywołania, które są wywoływane przez metody metody pod karetką (punktu wstawiania).  

 ![Okno hierarchii wywołań](../ide/media/VSIDE_call_hierarchy.png)

-  [CodeLens](../ide/find-code-changes-and-other-history-with-codelens.md) umożliwia znalezienie odwołań i zmiany kodu, połączonych usterek, elementy robocze, przeglądy kodu i testów jednostkowych wszystko to bez opuszczania edytora.  

 ![CodeLens](../ide/media/codelensoverview.png)

-  [Wgląd do definicji](../ide/how-to-view-and-edit-code-by-using-peek-definition-alt-plus-f12.md) okno zawiera wbudowany definicję metody lub typu, bez konieczności opuszczania bieżący kontekst.  

 ![Wgląd do definicji](../ide/media/VSIDE_peek_definition.png)

-  **Przejdź do definicji** menu kontekstowego przejście bezpośrednio do miejsca, w którym zdefiniowana jest funkcji lub obiektu. Inne polecenia nawigacji dostępne są także klikając prawym przyciskiem myszy w edytorze.  

 ![Przejdź do definicji](../ide/media/VSIDE_go_to_definition.png)

- Pokrewne narzędzia [przeglądarki obiektów](http://msdn.microsoft.com/f89acfc5-1152-413d-9f56-3dc16e3f0470), umożliwia można przeprowadzać inspekcję zestawy .NET lub środowiska wykonawczego systemu Windows w systemie, aby zobaczyć typy one zawierać a jakie elementy członkowskie (właściwości, metody, zdarzenia, itp.) tych typów.

  ![System.Timer w przeglądarce obiektów](../ide/media/objectbrowser.png)  

## <a name="manage-your-source-code-and-collaborate-with-others"></a>Zarządzanie kodu źródłowego i współpracę z innymi osobami
Możesz zarządzać kodu źródłowego w obsługiwanych przez dowolnego dostawcy, w tym GitHub repozytoriów Git. Lub użyj [programu Visual Studio Team Services (VSTS)](https://www.visualstudio.com/team-services/) do zarządzania kodu obok usterek i elementy pracy dla całego projektu. Zobacz [wprowadzenie do usługi Git i usługi Team Services](https://www.visualstudio.com/en-us/docs/git/gitquickstart-vs2017) Aby dowiedzieć się więcej o zarządzaniu repozytoriów Git w programie Visual Studio przy użyciu programu Team Explorer.  Visual Studio ma również inne funkcje kontroli źródła wbudowanych. Aby dowiedzieć się więcej o nich, zobacz [nowe funkcje Git w programie Visual Studio 2017 (blog)](https://blogs.msdn.microsoft.com/visualstudioalm/2017/03/06/new-git-features-in-visual-studio-2017/).  

Visual Studio Team Services to usługa oparta na chmurze dla hostingu oprogramowania projektów i umożliwianie współpracy w zespołach. VSTS obsługuje systemów zarówno Git i kontroli źródła programu Team Foundation, a także Scrum, CMMI i Agile metodologii programowanie. Team Foundation wersji formantu (TFVC) używa pojedynczy serwer scentralizowane repozytorium do śledzenia i wersji plików. Lokalne zmiany są zawsze ewidencjonowane na centralnym serwerze, gdy inni deweloperzy mogą pobrać najnowsze zmiany.  

Team Foundation Server (TFS) jest Centrum zarządzania cyklem życia aplikacji dla programu Visual Studio. Dzięki temu wszyscy pracownicy z procesem tworzenia do udziału za pomocą jednego rozwiązania. TFS jest przydatne w przypadku za zarządzanie heterogenicznym zespołów i projektów.  

Jeśli masz konto usługi Visual Studio Team Services lub Team Foundation Server w sieci, należy się z nim połączyć za pomocą programu Team Explorer okna w programie Visual Studio. Z tego okna można sprawdzić kod do lub z kontroli źródła, zarządzania elementami pracy, kompilacji i rozpoczęcia pokoje zespołów dostępu oraz obszarów roboczych. Możesz otworzyć Team Explorer z **Szybkie uruchamianie** okno, lub w menu głównym z **widok, Team Explorer** lub **zespołu, zarządzanie połączeniami**.  

Na poniższej ilustracji przedstawiono okno programu Team Explorer rozwiązania, które znajduje się w VSTS.  

![Program Visual Studio Team Explorer](../ide/media/vs2017_teamexplorer.png)  

Aby uzyskać więcej informacji na temat programu Visual Studio Team Services, zobacz [Visual Studio Team Services](https://www.visualstudio.com/team-services/). Aby uzyskać więcej informacji na temat programu Team Foundation Server, zobacz [Team Foundation Server](https://www.visualstudio.com/products/tfs-overview-vs).  

## <a name="connect-to-services-databases-and-cloud-based-resources"></a>Nawiązanie połączenia usługi, baz danych i zasobów w chmurze
Chmura ma kluczowe znaczenie dla współczesnych świata w trybie online, a program Visual Studio udostępnia środki do wykorzystania go. Na przykład funkcja usług połączonych umożliwia łączenie aplikacji z usługi. Aplikacje służy do przechowywania danych w magazynie Azure, między innymi.  

![Podłączonych usług](../ide/media/VSIDE_Tour_Connected_Services.png)

Wybieranie usługi na **usług połączonych** strony uruchomienie połączone Kreatora usługi, który służy do konfigurowania projektu i pliki do pobrania wymaganych pakietów NuGet i ułatwiają rozpoczęcie pracy kodowania z usługą.  

Można wyświetlić i zarządzać zasobami w chmurze bazujących na platformie Azure w ramach programu Visual Studio przy użyciu [Eksplorator chmury](/azure/vs-azure-tools-resources-managing-with-cloud-explorer). Eksplorator chmury zawiera zasoby platformy Azure w ramach kont zarządzanych w ramach subskrypcji Azure, które są rejestrowane w. Eksplorator chmury można uzyskać, wybierając **Azure programowanie** obciążenia w Instalatorze programu Visual Studio.  

![Eksplorator chmury](../ide/media/VSIDE_CloudExplorer.png)

**W Eksploratorze serwera** ułatwia przeglądanie i zarządzanie wystąpień programu SQL Server i zasobami lokalnie, zdalnie i na witryny Salesforce.com, Office 365, Azure i witryn sieci Web. Aby otworzyć Eksploratora serwera, w menu głównym, wybierz **widoku**, **Eksploratora serwera**. Zobacz [dodać nowe połączenia](https://docs.microsoft.com/visualstudio/data-tools/add-new-connections) Aby uzyskać więcej informacji na temat używania Eksploratora serwera.

[SQL Server Data Tools (SSDT)](https://docs.microsoft.com/sql/ssdt/download-sql-server-data-tools-ssdt) jest wydajne środowisko projektowe dla programu SQL Server, bazy danych SQL Azure i usługi Azure SQL Data Warehouse. Umożliwia tworzenie, debugowanie, obsługa i Refaktoryzuj baz danych. Możesz pracować z projektem bazy danych lub bezpośrednio z bazy danych połączonych wystąpienia na — lub poza siedzibą firmy.  

**Eksplorator obiektów SQL Server** w programie Visual Studio udostępnia widok obiektów bazy danych podobny do programu SQL Server Management Studio. Eksplorator obiektów SQL Server można wykonywać zadania zarządzania i projektowania lekkich bazy danych, takich jak edytowanie danych w tabeli, porównanie schematów, wykonywanie zapytań przy użyciu menu kontekstowe bezpośrednio w Eksploratorze obiektów SQL Server i inne.  

![Eksplorator obiektów SQL Server](../ide/media/vs2015_sqlobjectexplorer.png)  

## <a name="extend-visual-studio"></a>Rozszerzanie programu Visual Studio
Visual Studio nie ma dokładnie funkcji potrzebne, można dodać go! Można personalizowanie środowiska IDE są oparte na przepływie pracy i stylu, Dodaj obsługę dla zewnętrznych narzędzi nie została jeszcze zintegrowany z programem Visual Studio i modyfikować istniejące funkcje, aby zwiększyć wydajność. Visual Studio oferuje narzędzia, formantów i szablonów firmy Microsoft, partnerzy i społecznością. Aby dowiedzieć się więcej na temat rozszerzania programu Visual Studio, zobacz [rozszerzenia programu Visual Studio IDE](https://www.visualstudio.com/vs/extend/).  

## <a name="learn-more-and-find-out-whats-new"></a>Dowiedz się więcej i dowiedzieć się, jakie nowości
Jeśli nie znasz programu Visual Studio przed, obejrzyj [uzyskać pracy programowania z użyciem programu Visual Studio](../ide/get-started-developing-with-visual-studio.md), lub sprawdź bezpłatnych kursów Visual Studio na [Microsoft Virtual Academy](https://mva.microsoft.com/product-training/visual-studio-courses#!index=2&lang=1033). Jeśli chcesz wyewidencjonować nowe funkcje programu Visual Studio 2017, zobacz [What's New in Visual Studio 2017](../ide/whats-new-in-visual-studio.md).  

Gratulujemy ukończenia samouczka środowiska IDE programu Visual Studio! Mamy nadzieję, że znasz coś przydatne o pewnych jego najważniejszych funkcji.  

## <a name="see-also"></a>Zobacz także
* [Visual Studio IDE](https://www.visualstudio.com/vs/)
* [Pobieranie programu Visual Studio](https://www.visualstudio.com/downloads/)
* [Blog programu Visual Studio](https://blogs.msdn.microsoft.com/visualstudio/)
* [Fora programu Visual Studio](https://social.msdn.microsoft.com/Forums/vstudio/en-US/home?category=visualstudio%2Cvsarch%2Cvsdbg%2Cvstest%2Cvstfs%2Cvsdata%2Cvsappdev%2Cvisualbasic%2Cvisualcsharp%2Cvisualc)
* [Wirtualna Akademia firmy Microsoft](https://mva.microsoft.com/)
* [Channel 9](https://channel9.msdn.com/)