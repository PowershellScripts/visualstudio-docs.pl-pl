---
title: '&#39;Zwróć&#39; instrukcji poza funkcją | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT1018
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 03568f9f-5f4f-4a10-a738-9a73f3832b9e
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 07b633c87dc11b291a5a5783f8121b2a368996d6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49846521"
---
# <a name="39return39-statement-outside-of-function"></a>&#39;Zwróć&#39; instrukcji poza funkcją
Użyte `return` instrukcji w zakresie globalnym kodu. `return` Instrukcji powinna występować tylko w treści funkcji.  
  
 Wywoływanie funkcji z `()` operator jest wyrażeniem. Wszystkie wyrażenia mają wartości. `return` instrukcja jest używane do określenia wartości zwróconej przez funkcję. Ogólna postać jest:  
  
```  
  
return [ expression ];  
```  
  
 Gdy `return` instrukcja jest wykonywana, *wyrażenie* jest oceniana i zwracana jako wartość funkcji. Jeśli brak wyrażenia **niezdefiniowane** jest zwracana.  
  
 Zatrzymuje wykonywanie funkcji, kiedy `return` instrukcja jest wykonywana, nawet jeśli istnieją inne instrukcje jeszcze pozostało w treści funkcji. Wyjątkiem od tej reguły jest Jeśli **zwracają** występuje instrukcja w obrębie **spróbuj** bloku, i istnieje odpowiedni **na koniec** bloku, kod w  **na koniec** bloku zostaną wykonane, zanim funkcja zwróci.  
  
 Jeśli funkcja zwraca ponieważ osiągnie koniec treści funkcji bez wykonywania `return` instrukcji, wartość zwracana jest **niezdefiniowane** wartość (oznacza to wynik funkcji nie może być używany jako część większego wyrażenia ).  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Usuń `return` instrukcji od głównej części kodu (globalny zasięg).  
  
## <a name="see-also"></a>Zobacz też  
 [Return — instrukcja](../../javascript/reference/return-statement-javascript.md)   
 [Function — obiekt](../../javascript/reference/function-object-javascript.md)   
 [caller, właściwość (Function)](../../javascript/reference/caller-property-function-javascript.md)