---
title: "Okno narzędzi R pomocy dla programu Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 06/29/2017
ms.reviewer: 
ms.suite: 
ms.technology: devlang-r
ms.devlang: r
ms.tgt_pltfrm: 
ms.topic: get-started-article
ms.assetid: ef9c04d4-0d5e-405a-842e-8d47fa0e8781
caps.latest.revision: "1"
author: kraigb
ms.author: kraigb
manager: ghogen
ms.openlocfilehash: cf63def0503e885b1c6ab42584f9f1932b77127f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="help-in-r-tools-for-visual-studio"></a>Pomoc w R narzędzi dla programu Visual Studio

Pomoc dla R jest zintegrowana bezpośrednio okno interaktywne programu Visual Studio. Zawsze, gdy używana `?` polecenia, takich jak `?mtcars`, pomoc od dokumentacji R jest wyświetlany w oknie programu Visual Studio:

![Okno Pomoc w programie Visual Studio](media/help-window.png)

> [!Tip]
> W oknie Pomoc, podobnie jak wszystkie inne w programie Visual Studio można rozmieszczone i zadokowane, jednak chcesz. Zobacz [dostosowywanie układów okien w programie Visual Studio](../ide/customizing-window-layouts-in-visual-studio.md).
>
> Aby otworzyć Pomoc wyniki w przeglądarce, wybierz **R Narzędzia > Opcje** menu i zestaw **przeglądarki pomoc R** właściwości `External`. Zobacz [opcje](options.md).

Aby wyszukać Pomoc, użyj `??` polecenia następuje terminu wyszukiwania. Jeśli wyszukiwany termin zawiera spacje, użyj cudzysłowów:

```R
??"Motor Trend"
```

![Wyniki wyszukiwania pomocy](media/help-search1.png)

Okno Pomoc ma również pole wejściowe wyszukiwania za pomocą którego można przeprowadzić dalsze umożliwia wyszukiwanie w dokumentacji R bezpośrednio:

![Wyniki wyszukiwania pomocy przy użyciu pola wejściowego](media/help-search2.png)

## <a name="integrated-help-lookup"></a>Wyszukiwanie zintegrowane pomocy

Deweloperzy często wyszukiwanie w dokumentacji R, aby uzyskać pomoc dotyczącą nazwy funkcji, zestawy danych i innych elementów. R narzędzi dla programu Visual Studio (RTVS) usprawnia proces dzięki integracji wyszukiwania pomocy bezpośrednio w edytorze i interaktywne systemu windows.

- Naciśnięcie klawisza F1 podczas automatycznego zakończenia operacji tworzy lista wyników pomocy, które odpowiadają podciąg.
- Prawym przyciskiem myszy terminu wyszukiwania (takich jak funkcja) i wybierając **pomoc na temat** polecenie otwiera Pomoc dla tej funkcji. Można także wywoływać **pomoc na temat** dla dowolnego zaznaczenia.

    ![Wywoływanie pomoc za pośrednictwem menu kontekstowym kliknij prawym przyciskiem myszy](media/help-right-click.png)

> [!Tip]
> Aby otworzyć Pomoc zintegrowane w przeglądarce, wybierz **R Narzędzia > Opcje** i ustaw **przeglądarki sieci Web F1** do `External`. Zobacz [opcje](options.md).

## <a name="integrated-stackoverflow-search"></a>Wyszukiwanie zintegrowane StackOverflow

Oprócz wyszukiwanie w dokumentacji R, deweloperzy często wyszukiwania StackOverflow podczas pisania kodu. RTVS usprawnia również tego procesu. Kliknij prawym przyciskiem myszy termin lub zaznaczenie, wybierz opcję **Wyszukaj w sieci web dla** polecenia (Ctrl + F1) i Visual Studio powoduje otwarcie okna z wynikami wyszukiwania z zakresem StackOverflow:

![Wyniki wyszukiwania w sieci Web w programie Visual Studio](media/help-web-search-results.png)

Ciąg dołączany zakresu, można zmienić `R site:stackoverflow`, za pomocą **R Narzędzia > Opcje > F1 w sieci Web, ciąg wyszukiwania** opcji:

![Zmiana opcji ciąg wyszukiwania F1 w sieci Web](media/options-dialog.png)

Jeśli wolisz wyświetlić wyniki w przeglądarce, zmień **przeglądarki sieci Web F1** zgodnie z opisem w artykule na [opcje](options.md).