---
title: "Porady: śledzenie kodu dostosowując pasek przewijania | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a9ebe7ec-4b6f-4ba2-a79e-80fab3db485b
caps.latest.revision: "5"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: e6dd6eab2d607d059967e89030ae92d34b407ff1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-track-your-code-by-customizing-the-scrollbar"></a>Porady: śledzenie kodu dostosowując pasek przewijania
Podczas pracy z plikami kodu długie, może być trudne do wszystko, co należy pamiętać. Można dostosować pasek przewijania okna kodu, aby zapewnić widok co się dzieje w kodzie.  
  
### <a name="to-show-annotations-on-the-scroll-bar"></a>Aby wyświetlić adnotacje paska przewijania  
  
1.  Pasek przewijania można skonfigurować do wyświetlenia zmian w kodzie, punkty przerwania, błędy i zakładki.  
  
     Otwórz **paska przewijania** strona Opcje (**narzędzia, opcje, Edytor tekstu. Wszystkie języki** lub określonego języka lub typ **paska przewijania** w oknie Szybkie uruchamianie).  
  
2.  Wybierz **Pokaż adnotacje na pionowym pasku przewijania**, następnie wybierz adnotacje, aby wyświetlić. ( **Znaczniki** opcja zawiera punkty przerwania i zakładki.)  
  
3.  Teraz wypróbować jej możliwości. Otwórz plik kodu dużych i Zastąp element, który występuje w wielu miejscach w pliku. Pasek przewijania przedstawia wynik zamiany, więc można Wycofaj zmiany, jeśli element, który nie powinien być zastąpiony.  
  
     Poniżej przedstawiono wygląd paska przewijania po wyszukaj ciąg. Należy zauważyć, że są wyświetlane wszystkie wystąpienia ciągu.  
  
     ![Pasek przewijania po przeszukaniu ciągu. ] (../ide/media/enhancedscrollbarsearch.png "EnhancedScrollbarSearch")  
  
     Po wymianie wszystkie wystąpienia ciągu w tym miejscu jest pasek przewijania. Widać od razu, czy operacja spowodowała niektórych problemów.  
  
     ![Pasek przewijania po zastąpieniu ciąg z błędami](../ide/media/enhancedscrollbarreplace.png "EnhancedScrollbarReplace")  
  
### <a name="to-set-the-display-mode-for-the-scroll-bar"></a>Aby ustawić tryb wyświetlania dla paska przewijania  
  
1.  Pasek przewijania ma dwa tryby, tryb paska (ustawienie domyślne) i tryb mapy. Pasek tylko tryb Wyświetla wskaźniki adnotacji na pasku przewijania. W trybie mapy wiersze kodu są reprezentowane na pasku przewijania. Można wybrać, jak szeroka znajdują się i czy występują kodu źródłowego, gdy wskaźnik myszy znajduje się na nich. Po kliknięciu lokalizacji na pasku przewijania kursora przenosi do tej lokalizacji w kodzie. Zwinięte regiony są przyciemnione w różny sposób. są one rozwinięte je dwukrotnie.  
  
     Na **paska przewijania** opcji wybierz opcję **tryb użyj paska dla pionowego paska przewijania** lub **tryb Użyj mapy dla pionowego paska przewijania**. Można wybrać szerokość w **omówienie źródła** listy rozwijanej.  
  
     Oto przykład wyszukiwania wygląd mapy tryb jest włączony i szerokość jest ustawiona na wartość średnią:  
  
     ![Pasek przewijania w trybie mapy](../ide/media/enhancedscrollbar.png "EnhancedScrollbar")  
  
2.  W trybie mapy, aby włączyć Podgląd kodu po przeniesieniu kursora na pasku przewijania w górę i w dół, zaznacz **Pokaż etykietki narzędzia w wersji zapoznawczej** opcji. Oto, jak wygląda:  
  
     ![Pasek przewijania z etykietka narzędzia](../ide/media/enhancedscrollbarsearchtooltip.png "EnhancedScrollbarSearchTooltip")  
  
     Jeśli chcesz zachować tryb mapy przewijanie zachowanie i etykietki narzędzia w wersji zapoznawczej, ale nie chcesz przejrzeć kod źródłowy, możesz ustawić **omówienie źródła** do **poza**.