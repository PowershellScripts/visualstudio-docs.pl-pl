---
title: "Zamień zmiennej tymczasowej jego wartość w programie Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 01/26/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: ghogen
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: b66236847e597aeddb4e6f09c27e64e717fdb7d9
ms.sourcegitcommit: 205d15f4558315e585c67f33d5335d5b41d0fcea
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2018
---
# <a name="inline-a-temporary-variable-refactoring"></a>Wbudowanej zmiennej tymczasowej refaktoryzacji

Dotyczy to refaktoryzacji:

- C#

- Visual Basic

**Co:** umożliwia usunięcie zmiennej tymczasowej i zamienić ją na jej wartość.

**Kiedy:** użycie zmiennej tymczasowej sprawia, że kod jest trudne do zrozumienia.

**Dlaczego:** usuwanie zmiennej tymczasowej może poprawić czytelność kodu.

## <a name="how-to"></a>Porada

1. Zaznacz lub umieść kursor tekst wewnątrz zmiennej tymczasowej, aby był śródwierszowy:

   - C#:

    ![Wyróżniony kod - C#](media/inline-highlight-cs.png)

   - Visual Basic:

    ![Zaznaczony kod - języka Visual Basic](media/inline-highlight-vb.png)

1. Następnie wykonaj jedną z następujących czynności:

   - **Keyboard**
     - Naciśnij klawisz **Ctrl +.** Aby wyzwalacz **szybkie akcje i Refaktoryzacje** menu.
   - **Myszy**
     - Kliknij prawym przyciskiem myszy kod i wybierz **szybkie akcje i Refaktoryzacje** menu.

1. Wybierz **wbudowanej zmiennej tymczasowej** z menu podręcznego okna podglądu.

   Zmienna zostanie usunięty, a jego użycia zastąpiony wartością zmiennej.

   - C#:

    ![Wbudowany wynik - C#](media/inline-result-cs.png)

   - Visual Basic:

    ![Wynik wbudowanego - Visual Basic](media/inline-result-vb.png)

## <a name="see-also"></a>Zobacz także

[Refaktoryzacja](../refactoring-in-visual-studio.md)