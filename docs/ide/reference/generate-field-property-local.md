---
title: Generowanie pola, właściwości lub zmiennej lokalnej w programie Visual Studio
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 00e3f1d994c854bab319b6fec823fce213f4f2ba
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49822790"
---
# <a name="generate-a-field-property-or-local-variable-in-visual-studio"></a>Generowanie pola, właściwości lub zmiennej lokalnej w programie Visual Studio

Dotyczy to generowanie kodu:

- C#

- Visual Basic

**Co:** pozwala natychmiast generowania kodu dla wcześniej niezadeklarowany pola, właściwości lub lokalnego.

**Kiedy:** wprowadzenie nowego pola, właściwości lub lokalnej podczas wpisywania i aby poprawnie Zadeklaruj go automatycznie.

**Dlaczego:** można zadeklarować pola, właściwości lub lokalnej przed użyciem, jednak wygeneruje deklaracji i automatycznie wpisz tę funkcję.

## <a name="how-to"></a>Instrukcje

1. Umieść kursor w wierszu gdzie znajduje się czerwona fala. Czerwona fala wskazuje pola, lokalnej lub właściwości, które jeszcze nie istnieje.

   - C#:

       ![Wyróżniony kod C#](media/field-highlight-cs.png)

   - Visual Basic:

       ![Wyróżniony Kod VB](media/field-highlight-vb.png)

2. Następnie wykonaj jedną z następujących czynności:

   - **Keyboard**
      - Naciśnij klawisz **Ctrl**+**.** wyzwalacz **szybkie akcje i Refaktoryzacje** menu.
   - **Myszy**
      - Kliknij prawym przyciskiem myszy i wybierz **szybkie akcje i Refaktoryzacje** menu.
      - Umieść kursor nad czerwona fala, a następnie kliknij przycisk ![Żarówka](media/bulb-cs.png) ikona, który jest wyświetlany.
      - Kliknij ikonę ![Żarówka](media/bulb-cs.png) ikona, który pojawia się na lewym marginesie, jeśli kursor tekstu jest już w wierszu zawierającym czerwona fala.

      ![Generowanie pola/właściwości/elementu lokalnego (wersja zapoznawcza)](media/field-preview-cs.png)

3. Wybierz jedną z opcji generowania z menu rozwijanego.

   > [!TIP]
   > Użyj **podgląd zmian** link w dolnej części okna podglądu [Aby wyświetlić wszystkie zmiany](../../ide/preview-changes.md) , zostaną wprowadzone przed dokonaniem wyboru.

   Pola, właściwości lub lokalny jest tworzony z typu wywnioskowane z jej użycie.

   - C#:

       ![Generowanie metody powodują C#](media/field-result-cs.png)

   - Visual Basic:

       ![Generowanie metody powodują VB](media/field-result-vb.png)

## <a name="see-also"></a>Zobacz także

- [Generowanie kodu](../code-generation-in-visual-studio.md)
- [Podgląd zmian](../../ide/preview-changes.md)