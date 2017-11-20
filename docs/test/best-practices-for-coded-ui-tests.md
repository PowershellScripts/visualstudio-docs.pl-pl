---
title: "Najlepsze praktyki dotyczące kodowanych testów interfejsu użytkownika | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-test
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: coded UI tests, best practices
ms.assetid: d5aef766-a24c-4f1f-ac9b-e5462b6627d4
caps.latest.revision: "39"
ms.author: douge
manager: douge
ms.openlocfilehash: 76727d06b3f7c41436ae2939518986baba4b8e5c
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="best-practices-for-coded-ui-tests"></a>Najlepsze praktyki dotyczące kodowanych testów interfejsu użytkownika
Ten temat zawiera opis najlepszych rozwiązań, które należy wykonać podczas opracowywania kodowane testy interfejsu użytkownika.  
  
 **Wymagania**  
  
-   Visual Studio Enterprise  
  
## <a name="best-practices"></a>Najlepsze praktyki  
 Poniższe wskazówki umożliwiają utworzenie elastyczne kodowanego testu interfejsu użytkownika.  
  
-   Użyj **konstruktora kodowanego testu interfejsu użytkownika** zawsze, gdy jest to możliwe.  
  
-   Nie należy modyfikować `UIMap.designer.cs` pliku bezpośrednio. Jeśli to zrobisz, zmiany w pliku zostaną zastąpione.  
  
-   Tworzenie testu za pomocą sekwencji zarejestrowane metody. Aby uzyskać więcej informacji o sposobie rejestrowania metody, zobacz [tworzenie kodowanych testów interfejsu użytkownika](../test/use-ui-automation-to-test-your-code.md#VerifyingCodeUsingCUITCreate).  
  
-   Każda metoda zarejestrowane powinna działać na jednej stronie, formularzach i oknach dialogowych. Utworzenie nowej metody testu dla każdej nowej strony, formularzach i oknach dialogowych.  
  
-   Podczas tworzenia metody należy użyć nazwy metody znaczący zamiast domyślnej nazwy. Nazwę opisową pomaga w identyfikacji przeznaczenia metody.  
  
-   Jeśli to możliwe, należy ograniczyć każdej metody zarejestrowane do mniej niż 10 akcji. Takie podejście moduły ułatwia zastąpić metodę, w przypadku zmiany interfejsu użytkownika.  
  
-   Tworzenie przy użyciu każdego potwierdzenia **konstruktora kodowanego testu interfejsu użytkownika**, która automatycznie dodaje metody potwierdzenia do `UIMap.Designer.cs` pliku.  
  
-   Zmiany interfejsu użytkownika (UI), ponowne nagrać metody testowe lub metody potwierdzenia, czy ponowne nagrać poszczególnych sekcjach istniejące metody testowej.  
  
-   Utwórz oddzielne <xref:Microsoft.VisualStudio.TestTools.UITest.Common.UIMap.UIMap> pliku dla każdego modułu w testowanej aplikacji. Aby uzyskać więcej informacji, zobacz [testowanie dużej aplikacji przy użyciu wielu map UI](../test/testing-a-large-application-with-multiple-ui-maps.md).  
  
-   W testowanej aplikacji, użyj łatwy do rozpoznania nazwy podczas tworzenia formantów interfejsu użytkownika. Dzięki temu więcej znaczenie i użyteczność nazwy wygenerowanej automatycznie formantów.  
  
-   Jeśli tworzysz potwierdzenia przez kodowanie przy użyciu interfejsu API, tworzenie metody, dla każdego potwierdzenia w części <xref:Microsoft.VisualStudio.TestTools.UITest.Common.UIMap.UIMap> klasy, która znajduje się w `UIMap.cs` pliku. Tę metodę należy wywoływać z metodę testu do wykonania potwierdzenia.  
  
-   Jeśli są bezpośrednio kodowania, przy użyciu interfejsu API, użyj właściwości i metod w klasach wygenerowanych w `UIMap.Designer.cs` pliku w kodzie, jak można wykonywać następujące czynności. Te klasy spowoduje swoją pracę, łatwiejsze i bardziej niezawodne i mogą pomóc w bardziej wydajnej pracy.  
  
 Kodowane testy interfejsu użytkownika automatycznie dostosowania do dużej liczby zmian w interfejsie użytkownika. Jeśli na przykład element interfejsu użytkownika zmieniła położenie i kolor, w większości przypadków kodowanego testu interfejsu użytkownika będą nadal znaleźć poprawny element.  
  
 Podczas uruchomienia testu, kontrolek interfejsu użytkownika znajdują się przez strukturę testowania przy użyciu zestawu właściwości wyszukiwania, które są stosowane do każdej klasy formantu w definicjach utworzone przez **konstruktora testu kodowanego interfejsu użytkownika** w `UIMap.Designer.cs` pliku. Właściwości wyszukiwania zawiera pary nazwa wartość nazw właściwości i wartości właściwości, które mogą służyć do identyfikowania formantu, takich jak <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestControl.FriendlyName%2A>, <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestControl.Name%2A>, i <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestControl.ControlType%2A> właściwości formantu. Jeśli właściwości wyszukiwania nie uległy zmianie, kodowanego testu interfejsu użytkownika pomyślnie odnaleźć formantu w interfejsie użytkownika. Zmiana właściwości wyszukiwania kodowane testy interfejsu użytkownika mają algorytmu inteligentne dopasowania, który stosuje Algorytm heurystyczny można znaleźć kontrolki i systemu windows w interfejsie użytkownika. Po zmianie interfejsu użytkownika, można zmodyfikować właściwości wyszukiwania poprzednio zdefiniowane elementy, aby upewnić się, że zostały znalezione.  
  
## <a name="what-to-do-if-your-user-interface-changes"></a>Co robić w przypadku zmiany interfejsu użytkownika  
 Interfejsy użytkownika często zmieniają się podczas tworzenia. Poniżej przedstawiono kilka sposobów w celu ograniczenia wpływu tych zmian:  
  
-   Znajdź zarejestrowane metodę, która odwołuje się do tego formantu i użyj **konstruktora kodowanego testu interfejsu użytkownika** do ponownego rejestrowania akcji dla tej metody. Można użyć tej samej nazwie w metodzie zastąpić istniejące działania.  
  
-   Jeśli w kontrolce potwierdzenia, że nie jest już prawidłowy:  
  
    -   Usuń metodę, która zawiera potwierdzenia.  
  
    -   Usuń wywołanie tej metody z metody testowej.  
  
    -   Dodaj potwierdzenie nowego przeciągając przycisk krzyżyk na formantu interfejsu użytkownika, otwórz mapy interfejsu użytkownika i Dodaj nowe potwierdzenia.  
  
 Aby uzyskać więcej informacji o sposobie rejestrowania kodowanych testów interfejsu użytkownika, zobacz [Użyj interfejsu użytkownika do testów Your kodu automatyzacji](../test/use-ui-automation-to-test-your-code.md).  
  
## <a name="what-to-do-if-a-background-process-needs-to-complete-before-the-test-can-continue"></a>Co należy zrobić, jeśli proces w tle musi wykonać, zanim będzie można kontynuować testu  
 Może być konieczne poczekaj na zakończenie procesu, zanim będzie można kontynuować z następnej akcji interfejsu użytkownika. Można użyć w tym celu <xref:Microsoft.VisualStudio.TestTools.UITesting.PlaybackSettings.WaitForReadyLevel%2A> oczekiwania przed kontynuowaniem testu, jak w poniższym przykładzie.  
  
```  
// Set the playback to wait for all threads to finish  
Playback.PlaybackSettings.WaitForReadyLevel = WaitForReadyLevel.AllThreads;  
  
// Press the submit button  
this.UIMap.ClickSubmit();  
  
// Reset the playback to wait only for the UI thread to finish  
Playback.PlaybackSettings.WaitForReadyLevel = WaitForReadyLevel.UIThreadOnly;  
```  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.TestTools.UITest.Common.UIMap.UIMap>   
 <xref:Microsoft.VisualStudio.TestTools.UITesting>   
 [Używanie automatyzacji interfejsu użytkownika do testowania kodu](../test/use-ui-automation-to-test-your-code.md)   
 [Tworzenie kodowanych testów interfejsu użytkownika](../test/use-ui-automation-to-test-your-code.md#VerifyingCodeUsingCUITCreate)   
 [Testowanie dużej aplikacji przy użyciu wielu map UI](../test/testing-a-large-application-with-multiple-ui-maps.md)   
 [Obsługiwane konfiguracje oraz platformy zakodowanych testów interfejsu użytkownika i nagrywania akcji](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md)