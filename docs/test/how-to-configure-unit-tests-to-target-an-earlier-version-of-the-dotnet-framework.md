---
title: "Porady: Konfigurowanie testów jednostkowych pod kątem starszej wersji programu .NET Framework | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-test
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: adb6c011-5abd-41d2-8ead-08cd7579bf37
caps.latest.revision: "12"
ms.author: douge
manager: douge
ms.openlocfilehash: d7a899e16d79ba2aae40506eb3cd6739dcdb4397
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="how-to-configure-unit-tests-to-target-an-earlier-version-of-the-net-framework"></a>Porady: konfigurowanie testów jednostkowych pod kątem starszej wersji oprogramowania .NET Framework
Po utworzeniu projektu testu w programie Microsoft Visual Studio najnowszej wersji programu .NET Framework jest domyślnie jako element docelowy. Ponadto jeśli projekty testowe uaktualnienie poprzedniej wersji programu Visual Studio, ich uaktualnienia do najnowszej wersji programu .NET Framework. Edytując właściwości projektu, można jawnie ponownie docelowych projektu do wcześniejszych wersji programu .NET Framework.  
  
 Jednostki można tworzyć projekty testowe, które odnoszą się do określonych wersji systemu .NET Framework. Docelowa wersja musi być w wersji 3.5 lub nowszej, a nie może być wersji klienta. Program Visual Studio pozwala podstawowe obsługę testy jednostek, które odnoszą się do określonych wersji:  
  
-   Można tworzyć projektów testów jednostkowych i adresować je do określonej wersji programu .NET Framework.  
  
-   Można uruchomić testów jednostkowych kierowanych określonej wersji programu .NET Framework w programie Visual Studio na komputerze lokalnym.  
  
-   Testy jednostkowe można uruchomić kierowanych określonej wersji programu .NET Framework za pomocą MSTest.exe z wiersza polecenia.  
  
-   Testy jednostkowe można uruchamiać na agenta kompilacji podczas kompilacji.  
  
 **Testowanie aplikacji SharePoint**  
  
 Funkcje wymienione powyżej również umożliwia pisanie testów jednostkowych i integracji aplikacji programu SharePoint przy użyciu programu Visual Studio. [!INCLUDE[crabout](../test/includes/crabout_md.md)]jak tworzyć aplikacje programu SharePoint przy użyciu programu Visual Studio, zobacz [tworzenie rozwiązań programu SharePoint](/office-dev/office-dev/create-sharepoint-solutions), [kompilowanie i debugowanie rozwiązań SharePoint](/office-dev/office-dev/building-and-debugging-sharepoint-solutions) i [Weryfikowanie i debugowanie Kod programu SharePoint](/office-dev/office-dev/verifying-and-debugging-sharepoint-code).  
  
 **Ograniczenia**  
  
 Gdy ponownie docelowego Twoje projekty testowe do wcześniejszych wersji programu .NET Framework, obowiązują następujące ograniczenia:  
  
-   W .NET Framework 3.5 przeznaczanie dla wielu platform obsługuje projekty testowe, zawierające testy jednostkowe tylko. .NET Framework 3.5 nie obsługuje żadnego innego typu testu, takie jak kodowanego testu interfejsu użytkownika lub obciążenia. Ponownie celem jest zablokowana dla testu typu innego niż testy jednostkowe.  
  
-   Wykonywanie testów, które są przeznaczone dla wcześniejszych wersji programu .NET Framework jest obsługiwany tylko w domyślnego adaptera hosta. Nie jest obsługiwane na karcie hosta platformy ASP.NET. Aplikacji programu ASP.NET, które nie zostały uruchomione w kontekście ASP.NET Development Server muszą być zgodne z bieżącą wersją programu .NET Framework.  
  
-   Obsługa danych kolekcji jest wyłączone, po uruchomieniu testów, które obsługują przeznaczanie dla wielu platform .NET Framework 3.5. Można uruchomić pokrycia kodu za pomocą narzędzia wiersza polecenia programu Visual Studio.  
  
-   Testy jednostkowe, które używają programu .NET Framework 3.5 nie można uruchomić na komputerze zdalnym.  
  
-   Nie może wskazać testów jednostkowych do starszych wersji klienta platformy.  
  
### <a name="re-targeting-to-a-specific-version-of-the-net-framework-for-visual-basic-unit-test-projects"></a>Ponownego określenia wartości docelowej do określonej wersji programu .NET Framework dla projektów testów jednostkowych programu Visual Basic  
  
1.  Tworzenie nowego projektu testu jednostkowego języka Visual Basic. Na **pliku** menu, wybierz **nowy** , a następnie wybierz **projektu**.  
  
     **Nowy projekt** zostanie wyświetlone okno dialogowe.  
  
2.  W obszarze **zainstalowane szablony**, rozwiń węzeł **Visual Basic**. Wybierz **testu** , a następnie wybierz **projekt testowy** szablonu.  
  
3.  W **nazwa** polu tekstowym, wpisz nazwę dla języka Visual Basic projekt testowy, a następnie wybierz pozycję **OK**.  
  
4.  W Eksploratorze rozwiązań wybierz **właściwości** w menu skrótów nowy projekt testowy Visual Basic.  
  
     Są wyświetlane właściwości projekt testowy Visual Basic.  
  
5.  Na **skompilować** wybierz kartę **zaawansowane opcje kompilacji** jak pokazano na poniższej ilustracji.  
  
     ![Zaawansowane opcje kompilacji](../test/media/howtoconfigureunittest35frameworka.png "HowToConfigureUnitTest35FrameworkA")  
  
6.  Użyj **platformy docelowej (wszystkie konfiguracje)** listy rozwijanej, aby zmienić platformę docelową, aby **.NET Framework 3.5** lub nowszej wersji, jak pokazano na poniższej ilustracji, objaśnienia B. Nie należy określać wersji klienta.  
  
     ![Miejsce docelowe upuszczania framework &#45; w dół listy](../test/media/howtoconfigureunitest35frameworkstepb.png "HowToConfigureUniTest35FrameworkStepB")  
  
### <a name="re-targeting-to-a-specific-version-of-the-net-framework-for-visual-c-unit-test-projects"></a>Ponownego określenia wartości docelowej do określonej wersji programu .NET Framework dla programu Visual C# projektów testów jednostkowych  
  
1.  Tworzenie nowego projektu testu jednostkowego języka Visual C#. Na **pliku** menu, wybierz **nowy** , a następnie wybierz **projektu**.  
  
     **Nowy projekt** zostanie wyświetlone okno dialogowe.  
  
2.  W obszarze **zainstalowane szablony**, rozwiń węzeł **Visual C#**. Wybierz **testu** , a następnie wybierz **projekt testowy** szablonu.  
  
3.  W **nazwa** polu tekstowym, wpisz nazwę dla programu Visual C# projekt testowy, a następnie wybierz pozycję **OK**.  
  
4.  W Eksploratorze rozwiązań wybierz **właściwości** z menu skrótów nowego projektu testu Visual C#.  
  
     Są wyświetlane właściwości projekt testowy Visual C#.  
  
5.  Na **aplikacji** wybierz kartę **platformy docelowej** , a następnie wybierz **.NET Framework 3.5** lub nowszy z listy rozwijanej, aby zmienić framework.as docelowej pokazano na poniższej ilustracji. Nie należy określać wersji klienta.  
  
     ![Miejsce docelowe upuszczania framework &#45; w dół listy](../test/media/howtoconfigureunittest35frameworkcsharp.png "HowToConfigureUnitTest35FrameworkCSharp")  
  
### <a name="re-targeting-to-a-specific-version-of-the-net-framework-for-ccli-unit-test-projects"></a>Ponownego określenia wartości docelowej do określonej wersji programu .NET Framework dla języka C + +/ projektów testów jednostkowych interfejsu wiersza polecenia  
  
1.  Tworzenie nowego projektu testu jednostkowego języka C++. Na **pliku** menu, wybierz opcję **nowy** , a następnie kliknij przycisk **projektu**.  
  
     **Nowy projekt** zostanie wyświetlone okno dialogowe.  
  
    > [!WARNING]
    >  Aby utworzyć C + +/ testów jednostkowych interfejsu wiersza polecenia dla wcześniejszych wersji programu .NET framework dla programu Visual C++, należy użyć odpowiedniej wersji programu Visual Studio. Na przykład, aby skierować je do programu .NET Framework 3.5, należy zainstalować [!INCLUDE[vs_orcas_long](../debugger/includes/vs_orcas_long_md.md)] i [!INCLUDE[vs_orcas_long](../debugger/includes/vs_orcas_long_md.md)] dodatku Service Pack 1.  
  
2.  W obszarze **zainstalowane szablony**, rozwiń węzeł **Visual C ++**. Wybierz **testu** , a następnie wybierz **projekt testowy** szablonu.  
  
3.  W **nazwa** polu tekstowym, wpisz nazwę dla programu Visual C++ projekt testowy, a następnie kliknij przycisk **OK**.  
  
4.  W Eksploratorze rozwiązań wybierz **Zwolnij projekt** z projekt testowy Visual C++.  
  
5.  W Eksploratorze rozwiązań wybierz zwolniony projekt testowy Visual C++, a następnie wybierz **Edytuj \<Nazwa projektu > .vcxproj**.  
  
     Plik .vcxproj zostanie otwarty w edytorze.  
  
6.  Ustaw `TargetFrameworkVersion` w wersji 3.5 lub nowszej wersji w `PropertyGroup` etykietą `"Globals"`. Wersja klienta nie należy określać:  
  
    ```  
    <PropertyGroup Label="Globals">  
        <TargetName>DefaultTest</TargetName>  
        <ProjectTypes>{3AC096D0-A1C2-E12C-1390-A8335801FDAB};{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}</ProjectTypes>  
        <ProjectGUID>{CE16D77A-E364-4ACD-948B-1EB6218B0EA3}</ProjectGUID>  
        <TargetFrameworkVersion>3.5</TargetFrameworkVersion>  
        <Keyword>ManagedCProj</Keyword>  
        <RootNamespace>CPP_Test</RootNamespace>  
      </PropertyGroup>  
  
    ```  
  
7.  Zapisz i zamknij plik .vcxproj.  
  
8.  W Eksploratorze rozwiązań wybierz Zaznacz **Załaduj ponownie projekt** w menu skrótów projekt testowy Visual C++.  
  
## <a name="see-also"></a>Zobacz też  
 [Tworzenie i Uruchamianie testów jednostkowych dla istniejącego kodu](http://msdn.microsoft.com/en-us/e8370b93-085b-41c9-8dec-655bd886f173)   
 [Tworzenie rozwiązań programu SharePoint](/office-dev/office-dev/create-sharepoint-solutions)   
 [Kompilowanie i debugowanie rozwiązań SharePoint](/office-dev/office-dev/building-and-debugging-sharepoint-solutions)   
 [Okno dialogowe Ustawienia zaawansowane kompilatora (Visual Basic)](../ide/reference/advanced-compiler-settings-dialog-box-visual-basic.md)