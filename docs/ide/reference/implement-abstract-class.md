---
title: Implementuj klasę abstrakcyjną w programie Visual Studio
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 4da74a60741ac33143efd7aecf0a4275185b6d3b
ms.sourcegitcommit: 0a8ac5f2a685270d9ca79bb39d26fd90099bfa29
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/09/2018
ms.locfileid: "51294699"
---
# <a name="implement-an-abstract-class-in-visual-studio"></a>Implementuj klasę abstrakcyjną w programie Visual Studio

Dotyczy to generowanie kodu:

- C#

- Visual Basic

**Co:** umożliwia natychmiastowe wygenerowanie kodu wymaganego do implementacji klasy abstrakcyjnej.

**Kiedy:** ma być dziedziczona z klasy abstrakcyjnej.

**Dlaczego:** wszystkie abstrakcyjne składowe jeden po drugim, można zaimplementować ręcznie, ale tej funkcji będzie generowana automatycznie wszystkich podpisów metody.

## <a name="how-to"></a>Instrukcje

1. Umieść kursor w wierszu gdzie znajduje się czerwona fala wskazującą mają być dziedziczone z klasy abstrakcyjnej, ale nie zaimplementowano wszystkich wymaganych elementów członkowskich.

   - C#:

       ![Wyróżniony kod C#](media/abstract-highlight-cs.png)

   - Visual Basic:

       ![Wyróżniony Kod VB](media/abstract-highlight-vb.png)

2. Następnie wykonaj jedną z następujących czynności:

   - **Keyboard**
      - Naciśnij klawisz **Ctrl**+**.** wyzwalacz **szybkie akcje i Refaktoryzacje** menu.
   - **Myszy**
      - Kliknij prawym przyciskiem myszy i wybierz **szybkie akcje i Refaktoryzacje** menu.
      - Umieść kursor nad czerwona fala, a następnie kliknij przycisk ![Żarówka](media/bulb-cs.png) Ikona wyświetlana.
      - Kliknij ikonę ![Żarówka](media/bulb-cs.png) Ikona wyświetlana na lewym marginesie, jeśli kursor tekstu jest już w wierszu zawierającym czerwona fala.

   ![Implementowanie klasy w wersji zapoznawczej](media/abstract-preview-cs.png)

3. Wybierz **implementacji klasy abstrakcyjnej** z menu rozwijanego.

   > [!TIP]
   > - Użyj **podgląd zmian** link w dolnej części okna podglądu [Aby wyświetlić wszystkie zmiany](../../ide/preview-changes.md) , zostaną wprowadzone przed dokonaniem wyboru.
   > - Użyj **dokumentu**, **projektu**, i **rozwiązania** linki na dole okna (wersja zapoznawcza) do tworzenia podpisów właściwej metody w wielu klas, który dziedziczy z Klasa abstrakcyjna.

   Podpisy metody abstrakcyjne są tworzone i gotowe do zaimplementowania.

   - C#:

       ![Implementowanie klasy wynikC#](media/abstract-result-cs.png)

   - Visual Basic:

       ![Implementowanie klasy wynik VB](media/abstract-result-vb.png)

## <a name="see-also"></a>Zobacz także

- [Generowanie kodu](../code-generation-in-visual-studio.md)
- [Podgląd zmian](../../ide/preview-changes.md)