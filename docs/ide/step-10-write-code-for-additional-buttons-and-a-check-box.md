---
title: "Krok 10: Zapisywanie kodu dla dodatkowych przycisków i pola wyboru | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-acquisition
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 185cf370-ab39-4ac0-b6bc-601d5b95a4a2
caps.latest.revision: "21"
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 797b01016cb82aeb3d6ecfa1d11fa79df0085ee1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="step-10-write-code-for-additional-buttons-and-a-check-box"></a>Krok 10. Zapisywanie kodu dla dodatkowych przycisków i pola wyboru
Teraz możesz przystąpić do ukończenia cztery metody. Można skopiuj i wklej ten kod, ale jeśli chcesz dowiedzieć się najbardziej z tego samouczka, wpisz kod i użyj funkcji IntelliSense.  
  
 Ten kod dodaje funkcje do dodanego wcześniej przycisków. Bez tego kodu przycisków nie wykonuj żadnych czynności. Przyciski za pomocą kodu w ich `Click` zdarzenia (i używa pola wyboru `CheckChanged` zdarzeń) aby wykonać różne czynności, podczas aktywacji kontrolki. Na przykład `clearButton_Click` zdarzenie, które aktywuje po wybraniu **Wyczyść obraz** przycisku, powoduje usunięcie bieżącego obrazu, ustawiając jego `Image` właściwości `null` (lub, `nothing`). Każde zdarzenie w kodzie zawiera komentarze wyjaśniające, czego kod.  
  
 ![łącze do wideo](../data-tools/media/playvideo.gif "PlayVideo")wersję wideo tego tematu, zobacz [samouczek 1: Tworzenie podglądu obrazów w języku Visual Basic - 5 wideo](http://go.microsoft.com/fwlink/?LinkId=205216) lub [samouczek 1: Tworzenie podglądu obrazów w C# — wideo 5](http://go.microsoft.com/fwlink/?LinkId=205206). Tych klipów wideo korzysta z wcześniejszej wersji programu Visual Studio, dlatego są niewielkie różnice w niektórych poleceń menu i inne elementy interfejsu użytkownika. Jednak koncepcje i procedury działają podobnie w bieżącej wersji programu Visual Studio.  
  
> [!NOTE]
>  Jako najlepsze rozwiązanie: zawsze komentarzy kodu. Komentarze są informacje dla osoby w celu odczytu, a warto czasu w celu uczynienia kodu do zrozumienia. Wszystkie elementy w wierszu komentarz jest ignorowana przez program. Języka Visual C#, możesz dodać komentarz linii, wpisując dwa ukośniki na początku (/ /), a w języku Visual Basic komentarz linii, zaczynając od pojedynczego cudzysłowu (').  
  
### <a name="to-write-code-for-additional-buttons-and-a-check-box"></a>Pisanie kodu dla dodatkowych przycisków i pola wyboru  
  
-   Dodaj następujący kod do pliku kodu Form1 (pliku Form1.cs lub Form1.vb). Wybierz **VB** kartę, aby wyświetlić kod Visual Basic.  
  
     [!code-vb[VbExpressTutorial1Step9_10#2](../ide/codesnippet/VisualBasic/step-10-write-code-for-additional-buttons-and-a-check-box_1.vb)]
     [!code-csharp[VbExpressTutorial1Step9_10#2](../ide/codesnippet/CSharp/step-10-write-code-for-additional-buttons-and-a-check-box_1.cs)]  
  
### <a name="to-continue-or-review"></a>Aby kontynuować lub przeglądnąć  
  
-   Aby przejść do następnego kroku samouczka, zobacz [krok 11: Uruchom Program Your i spróbuj innych funkcji](../ide/step-11-run-your-program-and-try-other-features.md).  
  
-   Aby powrócić do poprzedniego kroku samouczka, zobacz [krok 9: Przejrzyj komentarz i kodu testu](../ide/step-9-review-comment-and-test-your-code.md).