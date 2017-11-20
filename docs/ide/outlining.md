---
title: Tworzenie konspektu | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- outlining
- Visual Studio, expand/collapse code
- Visual Studio, outlining
- expand/collapse code
- code [Visual Studio], outlining
- code [Visual Studio], hiding
- outlining code
ms.assetid: d1476758-9d35-4d74-b63c-310661932ecd
caps.latest.revision: "34"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: cc1b41f0b1095876129a9be451e5a1ff774c8dc5
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="outlining"></a>Tworzenie konspektu
Można ukryć kodu z widoku, zwijając region kodu, aby był on wyświetlany w obszarze znak plus (+). Możesz rozwinąć zwinięty region, klikając znak plus. (Lub naciśnij klawisz CTRL + M + M, aby zwinąć region, a następnie klawisz CTRL + M + M do rozwiń go ponownie.) Region zwijania można zwinąć również przez dwukrotne kliknięcie każdego wiersza w regionie na marginesie zwijania pojawia się po lewej kodu. Po umieszczeniu na zwinięty region, mogą wyświetlać zawartość obszaru zwinięte jako etykietka narzędzia.  
  
 Regiony zwijania marginesie są wyróżnione po umieszczeniu na marginesie przy użyciu myszy. Domyślnie wyróżnianie kolor może wydawać się raczej Blade w niektórych konfiguracjach kolorów. Możesz je zmienić w **narzędzia/Opcje/środowiska/czcionki i kolory/Collapsible Region**.  
  
 Podczas pracy w kodzie obramowane można rozwinąć sekcje, które chcesz pracować nad, zwijając, gdy są wykonywane, a następnie przenieść pozostałe sekcje zasad. Jeśli nie chcesz, aby mieć obramowanie wyświetlane, można użyć **zatrzymać zwijania** polecenie, aby usunąć informacje konspektu bez zakłócania kodu źródłowego.  
  
 **Cofnij** i **wykonaj ponownie** polecenia w **Edytuj** menu wpływać na te akcje. **Kopiowania**, **Wytnij**, **Wklej**, i Zachowaj operacji przeciągania i upuszczania zwijania informacji, ale nie zwijanej regionu. Na przykład przy kopiowaniu region, który jest zwinięte, **Wklej** operacji będzie Wklej skopiowany tekst jako rozwinięte region.  
  
> [!CAUTION]
>  Jeśli zmienisz obramowane region zwijania mogą zostać utracone. Na przykład usunięcia lub znajdowanie i zamienianie operacji może spowodować usunięcie koniec regionu.  
  
 Następujące polecenia można znaleźć w **edycji/zwijanie** podmenu.  
  
|||  
|-|-|  
|Ukryj zaznaczenia|(CTRL + M, CTRL + H) - zwija wybranego bloku kodu, który zwykle nie jest dostępna dla zwijania, na przykład `if` bloku. Aby usunąć regionu niestandardowego, użyj **zatrzymać ukrywanie bieżącego** (lub CTRL + M, CTRL + U). Nie jest dostępna w języku Visual Basic.|  
|Przełącz Tworzenie konspektu rozszerzenia|-Odwraca bieżący stan ukryte lub rozszerzonych najbardziej wewnętrzną funkcją zwijania sekcji, gdy kursor znajduje się w zagnieżdżonych zwiniętą sekcję.|  
|Przełącz wszystkie Tworzenie konspektu|(CTRL + M, CTRL + L) — zestawy wszystkie regiony do tej samej zwinięte lub rozszerzyć stanu. Jeśli niektóre regiony są rozwinięte, a niektóre zwinięte, następnie zwinięte regiony są rozwinięte.|  
|Zatrzymaj, obramowanie|(CTRL + M, CTRL + P) - usuwa wszystkie informacje zwijania w całym dokumencie.|  
|Przestań ukrywać bieżący|(CTRL + M, CTRL + U) - usuwa zwijania informacje dotyczące aktualnie wybranego regionu użytkownika. Nie jest dostępna w języku Visual Basic.|  
|Zwiń do definicji|(CTRL + M, CTRL + O) - Zwija wszystkie typy elementów członkowskich.|  
|Zwiń blok:\<granic logiczna >|(Visual C++) Zwija regionu w funkcji znajduje się punkt wstawiania. Na przykład jeśli punkt wstawiania znajduje się wewnątrz pętli, pętli jest ukryty.|  
|Zwiń wszystkie w: \<struktury logicznej >|(Visual C++) Zwija wszystkie struktury wewnątrz funkcji.|  
  
 Aby zdefiniować regionów tekst, który chcesz rozwiń lub Zwiń umożliwia także programu Visual Studio SDK. Zobacz [wskazówki: Tworzenie konspektu](../extensibility/walkthrough-outlining.md).