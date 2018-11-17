---
title: Wyświetl wartości w DataTips w edytorze kodu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 07/14/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugging [Visual Studio], DataTips
- DataTips tool
ms.assetid: ffa7bd18-439b-4685-a9b3-c7884b5de41f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: afb318c8aa327345b3cd76ee16b718db1e0386aa
ms.sourcegitcommit: 331dbb12e11fcd7f5d15fab05f3c861e48126e43
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/16/2018
ms.locfileid: "51826764"
---
# <a name="view-data-values-in-datatips-in-the-code-editor"></a>Podgląd wartości danych w DataTips w edytorze kodu
DataTips zapewniają wygodny sposób wyświetlania informacji na temat zmiennych w programie podczas debugowania. DataTips działa tylko w trybie przerwania i tylko w przypadku zmiennych, które znajdują się w bieżącym zakresie wykonywania. Jeśli po raz pierwszy, próbujących przeprowadzić debugowania kodu, warto przeczytać [tworzenie lepszych C# kodu za pomocą programu Visual Studio](../debugger/write-better-code-with-visual-studio.md) i [debugowania dla początkujących](../debugger/debugging-absolute-beginners.md) przed przejściem w tym artykule.
  
### <a name="to-display-a-datatip"></a>Aby wyświetlić etykietki danych  
  
1. Ustaw punkt przerwania, a następnie rozpocząć debugowanie (naciśnij klawisz **F5**).

2. W przypadku, gdy wstrzymaniu w debugerze, umieść wskaźnik myszy nad dowolnej zmiennej w bieżącym zakresie.
  
     Pojawi się DataTip.
  
3.  DataTip zniknie po usunięciu wskaźnika myszy. Aby przypiąć DataTip pozostaje otwarty, kliknij przycisk **Przypnij do źródła** ikony lub kliknij prawym przyciskiem myszy na zmiennej, następnie kliknij przycisk **Przypnij do źródła**.

    ![Przypinanie etykietki danych](../debugger/media/dbg-tips-data-tips-pinned.png "PinningDataTip")

    > [!NOTE]
    > Porady dotyczące danych są zawsze obliczane w kontekście, w przypadku, gdy wykonanie programu jest zawieszone, a nie w przypadku, gdy kursor znajduje się. Po umieszczeniu wskaźnika myszy nad zmienną w innej funkcji o tej samej nazwie jako zmiennej, która znajduje się w bieżącym kontekście, wartość zmiennej w innych funkcji jest wyświetlany jako wartość zmiennej w bieżącym kontekście.
  
### <a name="to-unpin-a-datatip-and-make-it-float"></a>Odepnij poradzie dotyczącej danych i liczb zmiennoprzecinkowych  
  
-   Etykietki danych przypięte, kliknij **Odepnij od źródła** ikony.  
  
     Ikona zmiany kodu pin nieprzypięte pozycji. DataTip jest teraz wyświetlany powyżej wszelkie otwarte okna. Zmiennoprzecinkowe DataTip zamyka podczas kończenia sesji debugowania.  
  
### <a name="to-repin-a-floating-datatip"></a>Aby repin zmiennoprzecinkowy etykietki danych  
  
-   W poradzie dotyczącej danych kliknij ikonę pinezki.  
  
     Ikona zmiany kodu pin przypiętych pozycji. Jeśli DataTip jest poza oknem źródła, ikonę pinezki jest wyłączona i nie można przypiąć DataTip.  
  
### <a name="to-close-a-datatip"></a>Aby zamknąć etykietki danych  
  
-   Umieść wskaźnik myszy nad etykietki danych, a następnie kliknij przycisk **Zamknij** ikony.  
  
### <a name="to-close-all-datatips"></a>Aby zamknąć wszystkie etykietki danych  
  
-   Na **debugowania** menu, kliknij przycisk **wyczyść wszystkie etykietki danych**.  
  
### <a name="to-close-all-datatips-for-a-specific-file"></a>Aby zamknąć wszystkie etykietki danych dla określonego pliku  
  
-   Na **debugowania** menu, kliknij przycisk **wyczyść wszystkie etykietki danych przypięte do** *pliku*.  
  
## <a name="expand-and-edit-information"></a>Rozwiń węzeł i edytować informacje o  
 Korzystanie z DataTips, aby rozwinąć tablica, struktury lub obiekt, aby wyświetlić jego składowe. Można również edytować wartość zmiennej w poradzie dotyczącej danych.  
  
#### <a name="to-expand-a-variable-to-see-its-elements"></a>Aby rozwinąć zmiennej, aby zobaczyć jego elementy  
  
-   W DataTip, umieść wskaźnik myszy **+** logowania, która znajduje się przed nazwę zmiennej.  
  
    Zmienna rozwijany, aby wyświetlić jego elementy w postaci drzewa.

    ![Wyświetl etykietki danych](../debugger/media/dbg-tour-data-tips.gif "wyświetlanie etykietki danych")
  
    Po rozwinięciu zmiennej, można przenieść w górę i w dół za pomocą klawiszy strzałek na klawiaturze. Alternatywnie można użyć myszy.  
  
#### <a name="to-edit-the-value-of-a-variable-using-a-datatip"></a>Aby edytować wartość zmiennej za pomocą etykietki danych  
  
1.  W poradzie dotyczącej danych kliknij wartość. Ta opcja jest wyłączona dla wartości tylko do odczytu.  
  
2.  Wpisz nową wartość, a następnie naciśnij klawisz ENTER.  
  
## <a name="making-a-datatip-transparent"></a>Ustawianie etykietki danych przezroczystości  
 Jeśli chcesz wyświetlić kod, który znajduje się za etykietki danych, istnieje możliwość DataTip tymczasowo przezroczysty. To nie dotyczy DataTips, które są przypięte lub zmiennoprzecinkową.  
  
#### <a name="to-make-a-datatip-transparent"></a>Aby przezroczyste etykietki danych  
  
-   W DataTip naciśnij klawisz CTRL.  
  
     DataTip pozostanie przezroczyste, tak długo, jak przytrzymaj wciśnięty klawisz CTRL.  
  
## <a name="visualize-complex-data-types"></a>Wizualizuj złożone typy danych  
 Jeśli ikona lupy pojawi się obok nazwy zmiennej w poradzie dotyczącej danych, co najmniej jeden [wizualizatorów](../debugger/create-custom-visualizers-of-data.md), takich jak [ciągu wizualizatorów](../debugger/string-visualizer-dialog-box.md), są dostępne dla zmiennych typu danych. Korzystanie z wizualizatora, aby wyświetlić informacje w sposób bardziej zrozumiały, zwykle graficznego.
  
#### <a name="to-view-the-contents-of-a-variable-using-a-visualizer"></a>Aby wyświetlić zawartość zmiennej za pomocą wizualizatora  
  
-   Kliknij na ikonę szkła powiększającego ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "ikonę Wizualizator") wybrać Wizualizator domyślna dla typu danych.  
  
     —lub—  
  
     Wyskakujące strzałki obok visualizer, aby wybrać z listy odpowiedni wizualizatorów typu danych.  
  
     Informacje wyświetlane wizualizatora.  
  
## <a name="add-information-to-a-watch-window"></a>Dodaj informacje do okna czujki  
 Jeśli chcesz nadal obejrzeć zmiennej w widoku listy można dodać zmienną **Obejrzyj** poradzie dotyczącej danych w oknie Pomoc.  
  
#### <a name="to-add-a-variable-to-the-watch-window"></a>Aby dodać zmienną w oknie czujki  
  
-   Kliknij prawym przyciskiem myszy etykietki danych, a następnie kliknij przycisk **Dodaj czujkę**.  
  
     Zmienna jest dodawany do **Obejrzyj** okna. Jeśli używasz wersji, która obsługuje wiele **Obejrzyj** systemu windows, zmienna jest dodawany do **Czujka 1.**  
  
## <a name="import-and-export-datatips"></a>Importowanie i eksportowanie etykietki danych  
 Możesz wyeksportować etykietek danych do pliku XML, które mogą być udostępniane przez współpracowników lub edytować za pomocą edytora tekstów.  
  
#### <a name="to-export-datatips"></a>Aby wyeksportować etykietek danych  
  
1.  Polecenie menu Debuguj **Eksportuj etykietki danych**.  
  
     **Eksportuj etykietki danych** pojawi się okno dialogowe.  
  
2.  Przejdź do lokalizacji, w którym chcesz zapisać plik XML, wpisz nazwę dla pliku przy użyciu standardowych plikowych technik **nazwy pliku** , a następnie kliknij przycisk **OK**.  
  
#### <a name="to-import-datatips"></a>Aby zaimportować etykietek danych  
  
1.  Polecenie menu Debuguj **Importuj etykietki danych**.  
  
     **Importuj etykietki danych** pojawi się okno dialogowe.  
  
2.  Użyj okna dialogowego, aby znaleźć plik XML, który chcesz otworzyć, a następnie kliknij przycisk **OK**.  
  
## <a name="see-also"></a>Zobacz też  
 [Co to jest debugowanie?](../debugger/what-is-debugging.md)  
 [Tworzenie lepszych C# kodu za pomocą programu Visual Studio](../debugger/write-better-code-with-visual-studio.md)  
 [Pierwsze spojrzenie na profilowanie](../debugger/debugger-feature-tour.md) [wyświetlanie danych w debugerze](../debugger/viewing-data-in-the-debugger.md)   
 [Wyrażenie kontrolne i QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Tworzenie niestandardowych wizualizatorów](../debugger/create-custom-visualizers-of-data.md)   