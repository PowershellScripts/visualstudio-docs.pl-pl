---
title: Implementuje interfejs w programie Visual Studio | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 01/26/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.topic: article
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload:
- dotnet
ms.openlocfilehash: ebcdad47ebb8ecae9d943acd8e0db60c20ef8378
ms.sourcegitcommit: 205d15f4558315e585c67f33d5335d5b41d0fcea
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2018
---
# <a name="implement-an-interface-in-visual-studio"></a>Zaimplementuj interfejs w programie Visual Studio

Dotyczy to generowanie kodu:

- C#

- Visual Basic

**Co:** umożliwia natychmiast generowania kodu wymaganego do implementacji interfejsu.

**Kiedy:** ma być dziedziczona z interfejsu.

**Dlaczego:** ręcznie można zaimplementować interfejsu wszystkich jeden po drugim, jednak funkcja ta automatycznie wygeneruje wszystkie podpisy — metoda.

## <a name="how-to"></a>Porada

1. Umieść kursor w wierszu przypadku red wężyk, który wskazuje ma odwołanie do interfejsu, ale nie zostały zaimplementowane wszystkich wymaganych elementów członkowskich.

   - C#:

    ![Wyróżniony kod C#](media/interface-highlight-cs.png)

   - Visual Basic:

    ![Wyróżniony Kod VB](media/interface-highlight-vb.png)

1. Następnie wykonaj jedną z następujących czynności:

   - **Keyboard**
     - Naciśnij klawisz **Ctrl +.** Aby wyzwalacz **szybkie akcje i Refaktoryzacje** menu.
   - **Myszy**
     - Kliknij prawym przyciskiem myszy i wybierz **szybkie akcje i Refaktoryzacje** menu.
     - Umieść kursor nad czerwona falista, a następnie kliknij przycisk ![Żarówka](media/bulb-cs.png) ikonę, która jest wyświetlana.
     - Kliknij przycisk ![Żarówka](media/bulb-cs.png) ikonę, która jest wyświetlana na lewym marginesie, gdy kursor tekstu jest już w wierszu zawierającym czerwona falista.

1. Wybierz **implementuj interfejs** z menu rozwijanego.

   ![Zaimplementuj interfejs podglądu](media/interface-preview-cs.png)

   > [!TIP]
   > - Użyj **podgląd zmian** łącze umieszczone u dołu okna podglądu [aby zobaczyć wszystkie zmiany](../../ide/preview-changes.md) która zostanie podjęta przed dokonaniem wyboru.
   > - Użyj **dokumentu**, **projektu**, i **rozwiązania** łącza w dolnej części okna podglądu do tworzenia podpisów odpowiedniej metody w wielu klas, które implementują interfejs.

   Podpisy metod interfejsu jest tworzony i jest gotowy do zaimplementowania.

   - C#:

      ![Zaimplementuj interfejs wynik C#](media/interface-result-cs.png)

   - Visual Basic:

      ![Zaimplementuj interfejs wynik VB](media/interface-result-vb.png)

   > [!TIP]
   > (C# tylko) Użyj **jawnie implementować interfejs** opcję, aby każdy poprzedzony wygenerowanej metody o nazwie interfejs w celu uniknięcia konfliktów nazw.
   >
   > ![Implementowanie interfejsu jawnie wyniku.](media/interface-explicitresult-cs.png);

## <a name="see-also"></a>Zobacz także

[Generowanie kodu](../code-generation-in-visual-studio.md)  
[Podgląd zmian](../../ide/preview-changes.md)