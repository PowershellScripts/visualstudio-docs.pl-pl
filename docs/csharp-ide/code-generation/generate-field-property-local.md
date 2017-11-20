---
title: "Generowanie pola, właściwości lub lokalnej - generowania kodu (C#) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/16/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c11888e0-31b1-44cc-9037-98d3f8b3623b
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7304ad001b5e5c26594c147f4ffc416c9ee539c2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="generate-a-field-property-or-local-in-c"></a>Generowanie pola, właściwości lub lokalnych w języku C# #
**Co:** umożliwia natychmiast generowania kodu dla poprzednio niezadeklarowany pola, właściwości lub lokalnego. 

**Kiedy:** wprowadzenie nowego pola, właściwości lub lokalnego podczas pisania i aby poprawnie zadeklarować, automatycznie.  

**Dlaczego:** przed użyciem, jednak ta funkcja zostanie Generowanie deklaracji i wpisz automatycznie można zadeklarować pola, właściwości lub lokalnego. 

**Jak:**

1. Umieść kursor w wierszu przypadku czerwona falista wskazujący użyto pola, lokalne lub właściwości, które jeszcze nie istnieje.

   ![Wyróżniony kod](media/field_highlight.png)

1. Następnie wykonaj jedną z następujących czynności:
   * **Klawiatury**
     * Naciśnij klawisz **Ctrl +.** Aby wyzwalacz **szybkie akcje i Refaktoryzacje** menu i wybierz **wygenerować pola/właściwości/lokalnego** z menu podręcznego okna podglądu.
   * **Myszy**
     * Kliknij prawym przyciskiem myszy i wybierz **szybkie akcje i Refaktoryzacje** menu i wybierz **wygenerować pola/właściwości/lokalnego** z menu podręcznego okna podglądu.
     * Umieść kursor nad czerwona falista, a następnie kliknij przycisk ![Żarówka](media/bulb.png) ikonę, która jest wyświetlana.
     * Kliknij przycisk ![Żarówka](media/bulb.png) ikonę, która jest wyświetlana na lewym marginesie, gdy kursor tekstu jest już w wierszu zawierającym czerwona falista.

   ![Generowanie podglądu pola/właściwości/lokalnego](media/field_preview.png)

   >[!TIP]
   >Użyj [ **podgląd zmian** ](../../ide/preview-changes.md) łącze umieszczone u dołu okna podglądu, aby zobaczyć wszystkie zmiany wprowadzone przed dokonaniem wyboru.

1. Pola, właściwości lub lokalnej zostaną utworzone automatycznie z typem wywnioskować na podstawie jej użycia.

   ![Generowanie wyników pola/właściwości/lokalnego](media/field_result.png)

## <a name="see-also"></a>Zobacz też  
[Generowanie kodu (C#)](../code-generation-csharp.md)  
[Podgląd zmian](../../ide/preview-changes.md) 