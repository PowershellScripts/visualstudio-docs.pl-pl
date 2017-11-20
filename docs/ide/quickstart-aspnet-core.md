---
title: "Szybki Start: tworzenie pierwszej aplikacji sieci web platformy ASP.NET Core za pomocą programu Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 10/10/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-acquisition
ms.tgt_pltfrm: 
ms.topic: article
ms.devlang: csharp
ms.assetid: e173fb7d-c5bd-4568-ba0f-aa61913b3244
author: gewarren
ms.author: gewarren
manager: ghogen
dev_langs: CSharp
ms.openlocfilehash: e87c46d1d78fafdc629a9f08e0bd7afacc1e1f3f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="quickstart-use-visual-studio-to-create-your-first-aspnet-core-web-app"></a>Szybki Start: tworzenie pierwszej aplikacji sieci web platformy ASP.NET Core za pomocą programu Visual Studio
W tej 5 – 10 min wprowadzenie do programu Visual Studio zintegrowane środowisko programistyczne (IDE) utworzysz prostą aplikację sieci web platformy ASP.NET Core C#. Jeśli program Visual Studio nie został już zainstalowany, zainstaluj go bezpłatnie [tutaj](http://www.visualstudio.com).  

## <a name="create-a-project"></a>Tworzenie projektu
Najpierw utworzysz projekt aplikacji sieci web platformy ASP.NET Core. Typ projektu jest dostarczany z plików szablonów, które stanowią aplikacji sieci web funkcjonalności, zanim nawet dodano niczego!  

1. Otwórz program Visual Studio 2017 r.  

1. Na pasku menu u góry wybierz **pliku**, **nowy**, **projektu...** .  

1. W **nowy projekt** okno dialogowe, w lewym okienku rozwiń **Visual C#**, a następnie wybierz **.NET Core**. W środkowym okienku wybierz **aplikacji sieci Web platformy ASP.NET Core**, a następnie wybierz **OK**.   

     Jeśli nie widzisz **.NET Core** projektu szablonu, Anuluj poza **nowy projekt** okna dialogowego polu, a następnie na pasku menu u góry wybierz **narzędzia**, **Pobierz narzędzia i Funkcje...** . Uruchamia Instalator programu Visual Studio. Wybierz **ASP.NET i sieć web development** obciążenia, a następnie wybierz **Modyfikuj**.  

     ![Obciążenie platformy ASP.NET w Instalatorze programu VS](../ide/media/quickstart-aspnet-workload.png)  

1. W **nową aplikację sieci Web Core ASP.NET** okno dialogowe, wybierz opcję **ASP.NET Core 2.0** z górnego menu rozwijanego. (Jeśli nie widzisz **ASP.NET Core 2.0** na liście, zainstaluj go, wykonując **Pobierz** łącza, które powinny być wyświetlane w żółty pasek w górnej części okna dialogowego.) Wybierz **OK**.  

   ![Nowe dialogbox aplikacji sieci Web platformy ASP.NET Core](../ide/media/quickstart-aspnet-core20.png)  

## <a name="explore-the-ide"></a>Eksploruj IDE  
1. W **Eksploratora rozwiązań** narzędzi, rozwiń węzeł **stron** folder, a następnie wybierz **About.cshtml** aby otworzyć go w edytorze. Ten plik odpowiada stronę o nazwie **o** w aplikacji sieci web.  

1. W edytorze, wybierz `AboutModel` , a następnie naciśnij klawisz **F12** lub wybierz **przejdź do definicji** z menu kontekstowego (kliknij prawym przyciskiem myszy). To polecenie powoduje przejście do definicji `AboutModel` klasy C#.  

   ![Menu kontekstowe przejdź do definicji](../ide/media/quickstart-aspnet-gotodefinition.png)  

1. Następnie firma Microsoft będzie wyczyścić `using` dyrektywy w górnej części pliku przy użyciu skrótu simple. Wybierz dowolną wyszarzone poza dyrektyw using a [szybkie akcje](../ide/quick-actions.md) żarówki pojawi się na lewym marginesie lub pod karetką. Wybierz żarówkę, a następnie wybierz **usunąć niepotrzebne deklaracje Using**.  

     Niepotrzebne deklaracje Using są usuwane z pliku.  

1. W `OnGet()` metody, należy zmienić treść poniższy kod:  

 ```csharp
 public void OnGet()
 {
     string directory = Environment.CurrentDirectory;
     Message = String.Format("Your directory is {0}.", directory);
 }
 ```  

1. Zobaczysz dwóch faliste podkreślenie są wyświetlane w obszarze **środowiska** i **ciąg**, ponieważ te typy nie są w zakresie. Otwórz **listy błędów** narzędzi, aby wyświetlić błędy tej samej liście. (Jeśli nie widzisz **listy błędów** narzędzi wybierz **widoku**, **listy błędów** na pasku menu u góry.)  

   ![Lista błędów](../ide/media/quickstart-aspnet-errorlist.png)  

1. W oknie edytora umieść kursor na jednej osi, który zawiera błąd, a następnie wybierz żarówkę szybkie akcje na lewym marginesie. Z menu rozwijanego wybierz **przy użyciu systemu;** dodawania tej dyrektywy do góry pliku i napraw błędy.  

## <a name="run-the-application"></a>Uruchamianie aplikacji
1. Naciśnij klawisz **Ctrl + F5** do uruchomienia aplikacji, a następnie otwórz go w przeglądarce sieci web.  

1. W górnej części witryny sieci web, wybierz **o** wyświetlić komunikatu dodanych w katalogu `OnGet()` metodę **o** strony.  

1. Zamknij przeglądarkę sieci web.  

Gratulujemy Kończenie pracy tego przewodnika Szybki Start! Mamy nadzieję, że znasz nieco o środowiska IDE programu Visual Studio. Jeśli chcesz delve głębiej do jego możliwości, kontynuuj samouczek w **samouczki** sekcji spisu treści.  

## <a name="see-also"></a>Zobacz także   
[Wprowadzenie do języka C# i Visual Basic przy użyciu programu Visual Studio](getting-started-with-visual-csharp-and-visual-basic.md)
[wprowadzenie Razor strony platformy ASP.NET Core](/aspnet/core/tutorials/razor-pages/razor-pages-start)  