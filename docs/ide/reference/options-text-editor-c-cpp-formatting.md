---
title: Opcje, Edytor tekstu, C/C++, formatowanie | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.C/C++.Formatting.General
- VS.ToolsOptionsPages.Text_Editor.C%2fC%2b%2b.Formatting.General
dev_langs: C++
helpviewer_keywords: Text Editor Options dialog box, formatting
ms.assetid: cb6f1cbb-5305-48da-a8e8-33fd70775d46
caps.latest.revision: "16"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 081dc1215b0e8ac026455a5449761ce103c35551
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="options-text-editor-cc-formatting"></a>Opcje, edytor tekstu, C/C++, formatowanie
Pozwala zmienić domyślne zachowanie Edytora kodu podczas programowania w C lub C++.  
  
 Dostępu do tej strony, w **opcje** okno dialogowe, w lewym okienku rozwiń **Edytor tekstu**, rozwiń węzeł **C/C++**, a następnie kliknij przycisk **formatowanie** .  
  
> [!NOTE]
>  Na komputerze w poniższych instrukcjach mogą być wyświetlane inne nazwy i lokalizacje niektórych elementów interfejsu użytkownika programu Visual Studio. Te elementy są określane przez numer wersji Visual Studio oraz twoje ustawienia. Aby uzyskać więcej informacji, zobacz [personalizowanie środowiska IDE programu Visual Studio](../../ide/personalizing-the-visual-studio-ide.md).  
  
## <a name="cc-options"></a>Opcje C/C++  
 **Włącz automatyczne szybka podpowiedź**  
 Włącza lub wyłącza funkcję Szybkie informacje technologii IntelliSense.  
  
## <a name="inactive-code"></a>Kod nieaktywny  
 **Pokaż nieaktywnych bloków kodu**  
 Kod, który jest nieaktywny, ze względu na `#ifdef` deklaracje są kolorowane w inny sposób, aby ułatwić jego identyfikację.  
  
 **Wyłącz nieprzezroczystość nieaktywnego kodu**  
 Nieaktywny kod można zidentyfikować za pomocą kolorów zamiast przezroczystości.  
  
 **Procent nieprzezroczystość nieaktywnego kodu**  
 Można dostosować stopień krycia dla bloków nieaktywnego kodu.  
  
## <a name="indentation"></a>Wcięcie  
 **Wcięcie nawiasów klamrowych**  
 Można skonfigurować sposób wyrównania nawiasów klamrowych po naciśnięciu klawisza ENTER po rozpoczęciu blok kodu, na przykład funkcję lub a `for` pętli. Nawiasy klamrowe mogą być wyrównane względem pierwszego znaku bloku kodu lub wcięte.  
  
 **Automatyczne wcięcia na karcie**  
 Można skonfigurować, co się dzieje w bieżącym wierszu kodu po naciśnięciu klawisza TAB. Albo wiersz zostaje wcięty, albo zostaje wstawiony tabulator.  
  
## <a name="miscellaneous"></a>Inne  
 **Wyliczanie komentarzy w oknie Lista zadań**  
 Edytor może skanować otwarte pliki źródłowe pod kątem wstępnie określonych słów w komentarzach. Tworzy wpis w **listy zadań** okna dla dowolnego słowa kluczowe, które znajdzie.  
  
 **Wyróżnij zgodnych tokenów**  
 Gdy kursor znajduje się obok nawiasu klamrowego, edytor może wyróżnić pasujący nawias klamrowy, abyś mógł łatwiej wyróżnić odpowiedni kod.  
  
## <a name="outlining"></a>Tworzenie konspektu  
 **Trybu zwijania przy otwieraniu plików**  
 Po przywróceniu pliku do edytora tekstów można włączyć funkcję tworzenia konspektów. Aby uzyskać więcej informacji, zobacz [Tworzenie konspektu](../../ide/outlining.md). Gdy ta opcja jest zaznaczona, tworzenie konspektów jest włączone po otwarciu pliku.  
  
 **Automatyczne zwijanie bloków obszaru #pragma**  
 Gdy ta opcja jest wybrana i automatyczne tworzenie konspektu dla [dyrektywy pragma](/cpp/preprocessor/pragma-directives-and-the-pragma-keyword) jest włączona. Dzięki temu można rozwinąć lub zwinąć bloki regionów pragmy w trybie konspektu.  
  
 **Automatyczne zwijanie bloków instrukcji**  
 Kiedy ta opcja jest zaznaczona, automatyczne tworzenie konspektu jest włączone dla następujących konsruktów instrukcji:  
  
-   [if-else](/dotnet/csharp/language-reference/keywords/if-else)  
  
-   [Switch — instrukcja (C++)](/cpp/cpp/switch-statement-cpp)  
  
-   [while — instrukcja (C++)](/cpp/cpp/while-statement-cpp)  
  
## <a name="see-also"></a>Zobacz też  
 [Ogólne, środowisko, opcje — Okno dialogowe](../../ide/reference/general-environment-options-dialog-box.md)   
 [Korzystanie z IntelliSense](../../ide/using-intellisense.md)