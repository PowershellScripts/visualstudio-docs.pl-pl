---
title: Generuj komentarze dokumentacji XML - generowania kodu (Visual Basic) | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/17/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d2025bd2-5984-4486-a61c-0a0933a735ea
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 1291667c7acb47abe543d275549179abea0c8467
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="generate-xml-documentation-comments-in-visual-basic"></a>Generuj komentarze dokumentacji XML w Visual Basic
**Co:** pozwala natychmiast wygenerować base XML wymagane do dokumentu wybranego elementu. 

**Kiedy:** chcesz utworzyć komentarzy dokumentu XML do późniejszego przetwarzania przez dokumentacji narzędzia, takiego jak Sandcastle.

**Dlaczego:** można ręcznie utworzyć blok komentarza całego samodzielnie, ale spowoduje to zaoszczędzić czas i zwiększyć dokładność, generując podstawowego szablonu i dodatkowych elementów. 

**Jak:**

1. Umieść kursor nad elementem chcesz dokumentu, na przykład metoda tekstu.

   ![Metoda do dokumentu](media/doc_highlight.png)

1. Następnie wpisz **'''** (3 pojedynczy cudzysłów) które automatycznie utworzy szablon podstawowy i wszelkie dodatkowe elementy w razie potrzeby.  Na przykład podczas dodawania komentarzy metody, generuje  **\<podsumowania\>**  tagi, jak również  **\<param\>**  tagu dla każdego parametru, który jest przekazywany do metody, a  **\<zwraca\>**  tag do dokumentu, metoda zwraca.

   ![Szablon](media/doc_preview.png)

1. Wypełnij komentarze i Dodaj wszelkie dodatkowe informacje, które można to konieczne.

   ![Komentarz ukończone](media/doc_result.png)

## <a name="see-also"></a>Zobacz też
[Dokumentowanie kodu za pomocą XML (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/documenting-your-code-with-xml)  
[Generowanie kodu (Visual Basic)](../code-generation-vb.md) 