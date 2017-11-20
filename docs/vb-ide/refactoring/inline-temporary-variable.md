---
title: Wbudowanej zmiennej tymczasowej - refaktoryzacji (Visual Basic) | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/17/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a63d6407-5acb-4d5f-8c0e-ecedddc07177
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 574a1a41464ede08571e1c0201618d666fa7ad92
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="inline-a-temporary-variable-in-visual-basic"></a>Wbudowanej zmiennej tymczasowej w języku Visual Basic
**Co:** umożliwia usunięcie zmiennej tymczasowej i zamień ją na rzeczywisty kod zamiast tego.

**Kiedy:** użycie zmiennej tymczasowej sprawia, że kod jest trudne do zrozumienia.  

**Dlaczego:** usuwanie zmiennej tymczasowej może czytelność kodu w niektórych sytuacjach

**Jak:**

1. Zaznacz lub umieść kursor tekst wewnątrz zmiennej tymczasowej, aby był śródwierszowy:

   ![Wyróżniony kod](media/inline_highlight.png)

1. Następnie wykonaj jedną z następujących czynności:
   * **Klawiatury**
     * Naciśnij klawisz **Ctrl +.** Aby wyzwalacz **szybkie akcje i Refaktoryzacje** menu i wybierz **wbudowanej zmiennej tymczasowej** z menu podręcznego okna podglądu.
   * **Myszy**
     * Kliknij prawym przyciskiem myszy kod, wybierz **szybkie akcje i Refaktoryzacje** menu i wybierz **wbudowanej zmiennej tymczasowej** z menu podręcznego okna podglądu.

   Zmienna zostanie usunięta i jego użycia zastąpiony wartością zmiennej natychmiast.

   ![Wynik wbudowany](media/inline_result.png)

## <a name="see-also"></a>Zobacz też
[Refaktoryzacji (Visual Basic)](../refactoring-vb.md)