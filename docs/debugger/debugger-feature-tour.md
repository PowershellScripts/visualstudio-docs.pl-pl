---
title: Debuger funkcji samouczek | Dokumentacja firmy Microsoft
ms.custom: H1HackMay2017
ms.date: 05/19/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: debugger
ms.assetid: c763d706-3213-494f-b4d2-990b6e1ec456
caps.latest.revision: "1"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b7edb1428d3dedbbe6341427e28964559d9750b1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="feature-tour-of-the-visual-studio-debugger"></a>Przewodnik po funkcji debuger programu Visual Studio

W tym temacie przedstawiono funkcje debugera programu Visual Studio. Jeśli chcesz z niego skorzystać, otwierając własną aplikację w programie Visual Studio, możesz to zrobić, lub można skorzystać z przykładowych aplikacji przy użyciu [przewodnik dla początkujących](../debugger/getting-started-with-the-debugger.md).

Funkcje opisane w tym miejscu są stosowane do języka C#, C++, Visual Basic, JavaScript i innych języków obsługiwanych przez program Visual Studio (inaczej w przypadku gdy).

## <a name="set-a-breakpoint-and-start-the-debugger"></a>Ustaw punkt przerwania i uruchomienia debugera

Aby debugować, należy uruchomić aplikację w debugerze procesu aplikacji. F5 (**Debuguj > Rozpocznij debugowanie**) jest najczęściej w tym celu. Jednak prawo teraz może nie wybrano żadnych punktów przerwania, aby zbadać aplikacji kodu, więc firma Microsoft będzie zrobić w pierwszej kolejności, a następnie uruchom debugowanie.

Jeśli plik jest otwarty w edytorze kodu można ustawić punktu przerwania, klikając na marginesie na lewo od wiersza kodu.

![Ustaw punkt przerwania](../debugger/media/dbg-tour-set-a-breakpoint.gif "Ustaw punkt przerwania")

Naciśnij klawisz F5 (**Debuguj > Rozpocznij debugowanie**) i debuger działa dla pierwszego punktu przerwania, który wykryje. Jeśli aplikacja nie jest jeszcze uruchomiona, F5 uruchomienie debugera i zatrzymuje się na pierwszym punktu przerwania.

Punkty przerwania są to przydatne, gdy wiesz, wiersz kodu lub części kodu, który ma zostać zbadany szczegółowo.

## <a name="navigate-code-in-the-debugger-using-step-commands"></a>Przejdź do kodu w debugerze przy użyciu poleceń krokowych

Udostępniamy skróty klawiaturowe dla większości poleceń, ponieważ ich nawigacji kodu aplikacji szybciej. (Odpowiednik polecenia takie jak polecenia menu są wyświetlane w nawiasach).

Aby uruchomić aplikację w debugerze, naciśnij klawisz F11 (**Debuguj > Wkrocz**). Jest F11 **Step Into** poleceń i zmienia aplikacji wykonanie jednej instrukcji w czasie. Po uruchomieniu aplikacji z F11 debuger dzieli się na pierwszej instrukcji, który jest wykonywany.

![F11 Wkrocz](../debugger/media/dbg-tour-f11.png "F11 wkroczyć do")

Żółta strzałka reprezentuje instrukcję, w której debuger wstrzymana, również wstrzymuje wykonywanie aplikacji w tym samym punkcie (Ta instrukcja nie wykonane).

F11 jest dobrym sposobem Sprawdź przepływ wykonania w najbardziej szczegółowy. (Aby szybciej niż przy użyciu kodu, możemy opisano niektóre inne opcje również.) Domyślnie debuger nakłada się na kodu innych użytkowników (Aby uzyskać więcej szczegółów, zobacz [tylko mój kod](../debugger/just-my-code.md)).

>[!NOTE]
> W kodzie zarządzanym zobaczysz okno dialogowe z pytaniem, jeśli chcesz otrzymać powiadomienie, gdy automatycznie wkroczyć nad właściwościami i operatorami (domyślnie). Jeśli chcesz zmienić ustawienie później, wyłącz **Przekrocz nad właściwościami i operatorami** w **Narzędzia > Opcje** menu w obszarze **debugowanie**.

## <a name="step-over-code-to-skip-functions"></a>Przekrocz nad kod, aby pominąć funkcji

Podczas pracy w wierszu kodu, który jest wywołanie metody lub funkcji, można nacisnąć klawisz F10 (**Debuguj > Step Over**) zamiast F11.

F10 wyjście z kodu bez Wkraczanie do funkcji lub metody w kodzie aplikacji (kod nadal wykonuje). Naciskając F10, można pominąć kod, który użytkownik nie chce w. W ten sposób szybki dostęp do kodu, która Cię interesuje więcej.

## <a name="step-into-a-property"></a>Wkraczać do właściwości

Jak wspomniano wcześniej, domyślnie debuger nakłada się na zarządzaną i pól, ale **Wkrocz do określonego** polecenie pozwala zmienić to zachowanie.

Kliknij prawym przyciskiem myszy na właściwości lub pola i wybierz polecenie **Wkrocz do określonego**, a następnie wybierz jedno z dostępnych opcji.

![Krok do określonego](../debugger/media/dbg-tour-step-into-specific.png "Wkrocz do określonego")

W tym przykładzie **Wkrocz do określonego** pobiera nam do kodu `Path.set`.

![Krok do określonego](../debugger/media/dbg-tour-step-into-specific-2.png "Wkrocz do określonego")

## <a name="run-to-a-point-in-your-code-quickly-using-the-mouse"></a>Uruchom do punktu w kodzie szybko za pomocą myszy

Znajduje się w debugerze, umieść kursor nad wiersz kodu do **Uruchom kliknięcie** przycisk (uruchamianie wykonywania tutaj) ![Uruchom kliknięcie](../debugger/media/dbg-tour-run-to-click.png "RunToClick") pojawia się po lewej stronie.

![Uruchom kliknięcie](../debugger/media/dbg-tour-run-to-click-2.png "Uruchom kliknięcie")

>  [!NOTE] 
> **Uruchom kliknięcie** przycisk (uruchamianie wykonywania tutaj) jest nowa w programie [!include[vs_dev15](../misc/includes/vs_dev15_md.md)].

Kliknij przycisk **Uruchom kliknięcie** przycisk (uruchamianie wykonywania tutaj). Debuger przechodzi do wiersza kodu, gdy kliknięto przycisk.

Za pomocą tego przycisku jest podobne do tymczasowego punktu przerwania. To polecenie jest również przydatna do poruszania się szybko w obrębie regionu widoczne kodu aplikacji. Można użyć **Uruchom kliknięcie** Otwieranie pliku.

## <a name="advance-the-debugger-out-of-the-current-function"></a>Poprawić debugera poza bieżącą funkcję

Czasami można kontynuować sesję debugowania, ale wcześniejszego debugera aż po bieżącej funkcji.

Naciśnij klawisze Shift + F11 (lub **Debuguj > Wyjdź**).

To polecenie wznawia wykonywanie aplikacji (i wyjście z kodu) do momentu zwraca bieżącej funkcji.

## <a name="run-to-cursor"></a>Uruchom do kursora

Zatrzymywanie działania debugera, naciskając klawisz **Zatrzymaj debugowanie** czerwony przycisk ![Zatrzymaj debugowanie](../debugger/media/dbg-tour-stop-debugging.png "Zatrzymaj debugowanie") lub Shift + F5.

Kliknij prawym przyciskiem myszy linię kodu w aplikacji i wybierz polecenie **Uruchom do kursora**. To polecenie uruchamia profilowanie i ustawia w bieżącym wierszu kodu tymczasowej punktu przerwania.

![Uruchom do kursora](../debugger/media/dbg-tour-run-to-cursor.png "Uruchom do kursora")

Jeśli ustawisz punktów przerwania, debuger wstrzymuje pierwszy punkt przerwania, który go trafienia.

Naciśnij klawisz F5, aż zostanie wyświetlony wiersz kodu po wybraniu **Uruchom do kursora**.

To polecenie jest przydatne podczas edytowania kodu i chcesz szybko ustawić punkt przerwania tymczasowego i uruchomienia debugera.


> [!NOTE]
> Można użyć **Uruchom do kursora** w **stos wywołań** okno podczas debugowania.

## <a name="restart-your-app-quickly"></a>Szybkie ponowne uruchomienie aplikacji

Kliknij przycisk **Uruchom ponownie** ![ponowne uruchomienie aplikacji](../debugger/media/dbg-tour-restart.png "ponowne uruchomienie aplikacji") przycisku w pasku narzędzi debugowania (**Ctrl + Shift + F5**).

Po naciśnięciu **ponowne uruchomienie**, można zaoszczędzić czas i zatrzymywanie aplikacji i ponowne uruchamianie debugera. Debuger wstrzymuje na pierwszy punkt przerwania, który zostaje trafiony za wykonywanie kodu.

Jeśli chcesz zatrzymać debuger i powrócić do edytora kodu, możesz nacisnąć przycisk Zatrzymaj red ![Zatrzymaj debugowanie](../debugger/media/dbg-tour-stop-debugging.png "Zatrzymaj debugowanie") przycisk zamiast **ponownego uruchomienia**.

## <a name="inspect-variables-with-data-tips"></a>Sprawdź zmienne etykietki danych

Teraz, znając nieco nawigację, masz możliwość uruchomienia sprawdzania stanu Twojej aplikacji (zmienne) z debugera. Funkcje, które pozwalają sprawdzić zmienne są niektóre najbardziej przydatne funkcje debugera, a istnieją różne sposoby, aby wykonać to zadanie. Często podczas debugowania problemu, próbujesz sprawdzić, czy zmienne są przechowywane wartości, które powinni być w stanie danej aplikacji.

Gdy wstrzymaniu w debugerze, umieść kursor nad obiektu przy użyciu myszy, aby zobaczyć wartość domyślną właściwości (w tym przykładzie nazwa pliku `market 031.jpg` jest wartością domyślną właściwości).

![Wyświetl etykietki danych](../debugger/media/dbg-tour-data-tips.gif "wyświetlenia etykietki danych")

Rozwiń obiekt, aby wyświetlić jego właściwości (takie jak `FullPath` właściwości w tym przykładzie).

Często podczas debugowania, chcesz szybko sprawdzić wartości właściwości obiektów i etykietki danych to dobry sposób, aby wykonać to zadanie.

> [!TIP]
> W większości obsługiwanych języków można edytować kodu w trakcie sesji debugowania. Aby uzyskać więcej informacji, zobacz [Edytuj i Kontynuuj](../debugger/edit-and-continue.md).

## <a name="inspect-variables-with-the-autos-and-locals-windows"></a>Sprawdź zmienne z automatycznych i ustawień regionalnych systemu windows

Podczas debugowania, obejrzyj **automatycznych** okna w dolnej części edytora kodu.

![Okno zmiennych automatycznych](../debugger/media/dbg-tour-autos-window.png "okno zmiennych automatycznych")

W **automatycznych** wyświetlane zmienne wraz z ich bieżącą wartość i ich typu. **Automatycznych** wszystkie zmienne używane w poprzednim wierszu lub bieżący wiersz zawiera okna (w języku C++ okna zawiera zmienne w poprzednim trzy wiersze kodu. Dokumentacji zachowanie specyficzne dla języka).

> [!NOTE]
> W języku JavaScript **zmiennych lokalnych** okna jest nie obsługiwane **automatycznych** okna.

Następnie przyjrzeć się **zmiennych lokalnych** okna. **Zmiennych lokalnych** okno zawiera zmiennych, które aktualnie znajdują się w zakresie.

![Okno zmiennych lokalnych](../debugger/media/dbg-tour-locals-window.png "okno zmiennych lokalnych")

W tym przykładzie `this` obiektu i obiekt `f` znajdują się w zakresie. Aby uzyskać więcej informacji, zobacz [sprawdzić zmiennych w automatycznych i zmiennych lokalnych Windows](../debugger/autos-and-locals-windows.md).

## <a name="set-a-watch"></a>Ustaw czujki

Można użyć **czujki** okna, aby określić zmienną (lub wyrażenie), który chcesz śledzić na.

Podczas debugowania, kliknij prawym przyciskiem myszy obiekt, a następnie wybierz pozycję **Dodaj wyrażenie kontrolne**.

![Okno czujki](../debugger/media/dbg-tour-watch-window.png "okno czujki")

W tym przykładzie ma czujki, ustawiać `File` obiekt, aby sprawdzić jego wartość zmienić podczas przeglądania przez debuger. W przeciwieństwie do innych zmiennych systemu windows **czujki** systemu windows zawsze pokazuj zmienne możesz obserwowanie (one jest wyszarzona kiedy poza zakresem).

Aby uzyskać więcej informacji, zobacz [ustawić czujki, przy użyciu czujki i QuickWatch systemu Windows](../debugger/watch-and-quickwatch-windows.md)

## <a name="examine-the-call-stack"></a>Sprawdź stosu wywołań

Kliknij przycisk **stos wywołań** okno podczas debugowania, które jest domyślnie otwarty w dolnym okienku po prawej stronie.

![Sprawdź stos wywołań](../debugger/media/dbg-tour-call-stack.png "zbadać stosu wywołań")

**Stos wywołań** okno zawiera kolejność, w którym są pobierania wywoływane metody i funkcje. Górny wiersz zawiera bieżącą funkcję ( `Update` metody w tym przykładzie). Drugi wiersz wskazuje, że `Update` została wywołana z `Path.set` właściwości i tak dalej. Stos wywołań jest dobrze do badania i zrozumienie przepływu wykonywania aplikacji.

> [!NOTE]
> **Stos wywołań** jest podobne do perspektywy debugowania w niektórych IDEs, takich jak Eclipse.

Możesz kliknąć dwukrotnie linię kod Przyjrzyj się tej kodu źródłowego i zmienia także bieżącego zakresu kontrolowanym przez debuger. To nie jest wcześniejsze debugera.

Można również użyć menu kliknij prawym przyciskiem myszy **stos wywołań** okno, aby wykonać inne czynności. Na przykład można wstawić punktów przerwania do określonych funkcji, uruchom komputer przy użyciu aplikacji **Uruchom do kursora**i przejść zbadanie kodu źródłowego. Zobacz [porady: zbadanie stosu wywołań](../debugger/how-to-use-the-call-stack-window.md).

## <a name="examine-an-exception"></a>Sprawdź Wystąpił wyjątek

Gdy aplikacja zgłasza wyjątek, debuger przejście do wiersza kodu, która zgłosiła wyjątek.
     
![Pomocnik wyjątków](../debugger/media/dbg-tour-exception-helper.png "pomocnika wyjątków")

W tym przykładzie **pomocnika wyjątków** pokazuje `System.Argument` wyjątku i komunikat o błędzie z informacją, że ścieżka nie jest niedozwolony format. Tak wiemy, że wystąpił błąd na argumentu metody lub funkcji.

W tym przykładzie `DirectoryInfo` wywołania nadać błąd na pusty ciąg, przechowywane w `value` zmiennej.

Pomocnik wyjątków jest doskonałym funkcja, która może pomóc w debugowaniu błędy. Można również wykonywać następujące czynności widoku Szczegóły błędu i Dodaj wyrażenie kontrolne pomocnika wyjątków. Lub, w razie potrzeby można zmienić warunki zgłaszanie określonego wyjątku.

>  [!NOTE] 
> Pomocnik wyjątków zastępuje Asystenta wyjątków w [!include[vs_dev15](../misc/includes/vs_dev15_md.md)].

Rozwiń węzeł **ustawienia wyjątków** węzeł, aby wyświetlić więcej opcji, w jaki sposób obsługiwać ten typ wyjątku, ale nie ma potrzeby zmian w tym samouczku!

## <a name="more-features-to-look-at"></a>Więcej funkcji, aby przyjrzeć się

-   [Debuger porady i wskazówki](../debugger/debugger-tips-and-tricks.md) Dowiedz się, jak zwiększyć wydajność pracy z debugera.

-   [Edytuj i Kontynuuj](../debugger/edit-and-continue.md) dla podzbioru języków (C#, C++, Visual Basic), funkcja Edytuj i Kontynuuj umożliwia edytowanie kodu w trakcie sesji debugowania.

-   [Debuguj aplikacje wielowątkowe](../debugger/debug-multithreaded-applications-in-visual-studio.md) opisano, jak można debugować aplikacji wielowątkowych. 

-   [Zdalne debugowanie](../debugger/remote-debugging.md) opisano, jak można debugować aplikacje działające na innych komputerach lub urządzeniach. 
  
-   [IntelliTrace](../debugger/intellitrace.md) zawiera opis funkcji IntelliTrace w Visual Studio Enterprise. Służy on do rejestrowania i śledzenia historii wykonywania kodu.

-   [Użycie sieci](../profiling/network-usage.md) opisuje profilowania narzędzie, które umożliwia debugowanie usług sieci web i innych zasobów sieciowych w systemie Windows aplikacji Uniwersalnej. Narzędzie do sprawdzenia ładunków.

-   [Debug Interface Access SDK](../debugger/debug-interface-access/debug-interface-access-sdk.md) opisuje debugowania programu Microsoft interfejsu dostępu Software Development Kit (DIA SDK). DIA SDK udostępnia informacje przechowywane w plikach bazy danych (.pdb) program wygenerowany przez Microsoft postcompiler narzędzia debugowania.  

## <a name="see-also"></a>Zobacz też  
 [Debugowanie w programie Visual Studio](../debugger/index.md)