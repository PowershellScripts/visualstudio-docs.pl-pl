---
title: Zastąp zmienną tymczasową wartość w programie Visual Studio
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: fb6fc6888e33b2cc0d210e9cb1e1aababe304f2a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49916767"
---
# <a name="inline-a-temporary-variable-refactoring"></a>Wbudowanej zmiennej tymczasowej refaktoryzacji

Ta Refaktoryzacja mają zastosowanie do:

- C#

- Visual Basic

**Co:** pozwala usunąć zmienną tymczasową i zamienić ją na jej wartość.

**Kiedy:** wykorzystanie zmiennej tymczasowej sprawia, że kod jest trudniejsze do zrozumienia.

**Dlaczego:** usuwanie zmiennej tymczasowej może poprawić czytelność kodu.

## <a name="how-to"></a>Instrukcje

1. Zaznacz lub umieść kursor tekstu w zmiennej tymczasowej, aby był śródwierszowy:

   - C#:

       ![Wyróżniony kod-C#](media/inline-highlight-cs.png)

   - Visual Basic:

       ![Wyróżniony kod - języka Visual Basic](media/inline-highlight-vb.png)

2. Następnie wykonaj jedną z następujących czynności:

   - **Keyboard**
      - Naciśnij klawisz **Ctrl**+**.** wyzwalacz **szybkie akcje i Refaktoryzacje** menu.
   - **Myszy**
      - Kliknij prawym przyciskiem myszy ten kod, a następnie wybierz pozycję **szybkie akcje i Refaktoryzacje** menu.

3. Wybierz **wstawiona zmienna tymczasowa** z menu podręcznego okna podglądu.

   Zmienna zostanie usunięty, a jego użycia zastępuje wartość zmiennej.

   - C#:

      ![Wynik wbudowane-C#](media/inline-result-cs.png)

   - Visual Basic:

      ![Wynik wbudowane - Visual Basic](media/inline-result-vb.png)

## <a name="see-also"></a>Zobacz także

- [Refaktoryzacja](../refactoring-in-visual-studio.md)