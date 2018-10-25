---
title: Zaawansowane opcje, Edytor tekstów, Basic (VB)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Visual_Basic.Editor
- VS.ToolsOptionsPages.Text_Editor.Basic.Editor
- VS.ToolsOptionsPages.Visual_Basic_Editor.Editor
- VS.ToolsOptionsPages.Text_Editor.Basic.SimplifiedEditorPage
- VS.ToolsOptionsPages.Text_Editor.Basic
- VS.ToolsOptionsPages.Text_Editor.Basic.Advanced
- VS.ToolsOptionsPages.Text_Editor.Basic.VB_Specific
helpviewer_keywords:
- Basic Text Editor Options dialog box
ms.assetid: 5a8cafca-f7b4-4a2d-92ce-6894a7673d00
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 994edc924d0261a7eb26c4eac6e3c9277f15a81c
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49823882"
---
# <a name="options-text-editor-basic-visual-basic-advanced"></a>Zaawansowane opcje, Edytor tekstów, Basic (Visual Basic)
**VB określonych** stronie właściwości, **podstawowe** folderu **edytora tekstów** folderu **opcje** (**narzędzia** menu) okno dialogowe zawiera następujące właściwości:

 **Włącz wyróżnianie odwołań i słów kluczowych**

Edytor tekstu można wyróżnić wszystkich wystąpień symbolu lub wszystkich słów kluczowych w klauzuli takich jak `If..Then`, `While...End While`, lub `Try...Catch...Finally`. Możesz przechodzić między do wyróżnionych odwołań lub słów kluczowych, naciskając klawisz **Ctrl** + **Shift** + **Strzałka w dół** lub **Ctrl**   +  **Shift** + **Strzałka w górę**.

**Włącz tryb konspektu**

Po otwarciu pliku w edytorze kodu, możesz wyświetlić dokument w trybie konspektu. Zobacz [konspekt](../../ide/outlining.md) Aby uzyskać więcej informacji. Gdy ta opcja jest zaznaczona, funkcję tworzenia konspektów jest aktywowany po otwarciu pliku.

**Pokaż separatory wierszy procedury**

Edytor tekstu wskazuje zakres visual procedur. Linia jest rysowana *.vb* pliki źródłowe projektu w lokalizacjach wymienione w poniższej tabeli:

|Lokalizacja w pliku źródłowym .vb|Przykład lokalizację wiersza|
|---------------------------------|------------------------------|
|Po zamknięciu bloku konstrukcja deklaracji|-Na końcu klasy, struktury, moduł, interfejs lub wyliczenie<br />-After właściwości, funkcji lub sub<br />-Nie między get i set klauzule we właściwości|
|Po zestaw konstrukcji w jednym wierszu|-After instrukcje importowania, przed definicją typu w pliku klasy<br />-After zmienne zadeklarowane w klasie, zanim wszelkie procedury|
|Po jednym wierszu deklaracji (-block deklaracje poziomu)|— Następujące instrukcje importu dziedziczy instrukcji, deklaracji zmiennych, deklaracji zdarzeń, delegat deklaracje i biblioteki DLL zadeklarować instrukcji|

 **Formatowania kodu (ponowne formatowanie) kodu** Edytor tekstu formatuje kodu zgodnie z potrzebami. Gdy ta opcja jest zaznaczona, Edytor kodu wykonują następujące czynności:

-   Wyrównaj kod do położenia odpowiedniej karcie

-   Recase słów kluczowych, zmienne i obiekty do odpowiedniej wielkości liter

-   Dodaj brakujące `Then` do `If...Then` — instrukcja

-   Dodaj nawiasy do wywołania funkcji

-   Dodaj brakujące nawiasy zakończenia na ciągi

-   Zapis wykładniczy formatowania

-   Ponowne formatowanie dat

**Automatyczne wstawianie konstrukcji końcowych**

 Podczas wpisywania — na przykład pierwszy wiersz deklaracja procedury `Sub Main—`i naciśnij klawisz **Enter**, Edytor tekstu dodaje pasujący obiekt typu `End Sub` wiersza. Podobnie jeśli dodasz [dla](/dotnet/visual-basic/language-reference/statements/for-next-statement) pętli, Edytor tekstu dodaje pasujący obiekt typu `Next` instrukcji. Gdy ta opcja jest zaznaczona, Edytor kodu automatycznie dodaje konstrukcja końcowa.

**Automatyczne wstawianie składowych Interface i MustOverride**

Jeśli zdecydujesz się `Implements` instrukcji lub `Inherits` instrukcji dla klasy, Edytor tekstu wstawia prototypy dla elementów członkowskich, które mają zostać zaimplementowane lub została zastąpiona, odpowiednio.

**Pokaż separatory wierszy procedury**

Edytor tekstu wskazuje zakres visual procedur. Linia jest rysowana w plikach źródłowych .vb projektu w lokalizacjach, wymienione w poniższej tabeli:

|Lokalizacja w pliku źródłowym .vb|Przykład lokalizację wiersza|
| - | - |
|Po zamknięciu bloku konstrukcja deklaracji|-Na końcu klasy, struktury, moduł, interfejs lub wyliczenie<br />-After właściwości, funkcji lub sub<br />-Nie między get i set klauzule we właściwości|
|Po zestaw konstrukcji w jednym wierszu|-After instrukcje importowania, przed definicją typu w pliku klasy<br />-After zmienne zadeklarowane w klasie, zanim wszelkie procedury|
|Po jednym wierszu deklaracji (-block deklaracje poziomu)|— Następujące instrukcje importu dziedziczy instrukcji, deklaracji zmiennych, deklaracji zdarzeń, delegat deklaracje i biblioteki DLL zadeklarować instrukcji|

**Włącz sugestie korekty błędów**

Edytor tekstu można zasugerować rozwiązania typowych problemów i pozwalają wybrać odpowiednią poprawkę, co jest następnie stosowane do kodu.

## <a name="see-also"></a>Zobacz też

- [Ogólne, Środowisko, Opcje — okno dialogowe](../../ide/reference/general-environment-options-dialog-box.md)
- [Opcje, Edytor tekstów, Wszystkie języki, Karty](../../ide/reference/options-text-editor-all-languages-tabs.md)