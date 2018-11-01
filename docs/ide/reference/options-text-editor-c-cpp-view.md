---
title: Wyświetl opcje, Edytor tekstu, C/C++
ms.date: 10/29/2018
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.C/C++.View
- VS.ToolsOptionsPages.Text_Editor.C%2FC%2B%2B.View
- VS.ToolsOptionsPages.Text_Editor.C\C++.View
author: mikeblome
ms.author: mblome
manager: wpickett
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.workload:
- cplusplus
ms.openlocfilehash: 9cf1cde04a45df47627b8b8bf9a0fad7b9bef0c4
ms.sourcegitcommit: be938c7ecd756a11c9de3e6019a490d0e52b4190
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2018
ms.locfileid: "50673738"
---
# <a name="options-text-editor-cc-view"></a>Wyświetl opcje, Edytor tekstu, C/C++

Użyj tych stron właściwości, aby zmienić domyślne zachowanie edytora kodu, podczas programowania w języku C lub C++.

Aby uzyskać dostęp do tej strony właściwości, wybierz **narzędzia** > **opcje** i rozwiń **Edytor tekstu**, następnie **C/C++**, a następnie wybierz pozycję **Widoku**.

> [!NOTE]
> Na komputerze w poniższych instrukcjach mogą być wyświetlane inne nazwy i lokalizacje niektórych elementów interfejsu użytkownika programu Visual Studio. Te elementy są określane przez numer wersji Visual Studio oraz twoje ustawienia. Zobacz [personalizowanie środowiska IDE programu Visual Studio](../../ide/personalizing-the-visual-studio-ide.md).

## <a name="code-squiggles"></a>Faliste linie kodu

Można włączać lub wyłączać następujących ustawień, aby zarządzać sposobem, w tekst, który Edytor obsługuje faliste linie kodu dla C i C++:

- **Makra w regionach pominięte przeglądania** — definiuje sposób wyróżnić makra, które znajdują się wewnątrz pominięto regionów za pomocą bazy danych przeglądania, takich jak makra, których definicje zawierają nawiasy klamrowe.

- **Makra można przekonwertować na constexpr** — definiuje sposób wyróżnić definicji makra, które mogą być konwertowane na `constexpr` definicje.

## <a name="inactive-code"></a>Kod nieaktywny

- **Pokaż nieaktywne bloki** -nieaktywne bloki preprocesora, jest pokolorowany inaczej.

- **Wyłącz nieprzezroczystość nieaktywnego kodu** — pełny kolor zamiast nieprzezroczystości, jest używany dla bloków nieaktywnego kodu.

- **Procent krycia nieaktywnego kodu** — procent krycia dla bloków nieaktywnego kodu.

## <a name="miscellaneous"></a>Różne

- **Wyliczanie zadań w komentarzach** — "open source" Skanuj pliki pod kątem tokenów programu VS i raportuj je w oknie Lista zadań.

- **Podświetl pasujące tokeny** — wyróżnienia otaczający nawiasy lub składnię, która pasuje, gdy kursor znajduje się. 

## <a name="outlining"></a>Tworzenie konspektu

- **Włącz konspekt** — przejdź do trybu konspektu po otwarciu pliku.

- **Konspekt obszarów Pragma** — automatyczne tworzenie konspektu `#pragma` bloki regionów.

- **Konspekt bloków instrukcji** — automatycznie konspekt bloków instrukcji.

## <a name="see-also"></a>Zobacz także

- [Ustawianie opcji edytora specyficznych dla języka](../../ide/reference/setting-language-specific-editor-options.md)
- [Refaktoryzacja języka C++ (VC Blog)](http://blogs.msdn.com/b/vcblog/archive/2014/11/14/all-about-c-refactoring-in-visual-studio-2015-preview.aspx)
