---
title: Wyliczenia Visual C++ w Projektancie klas | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Class Designer [Visual Studio], enumerations
ms.assetid: 11e90ba1-18cd-44f8-9e26-e3746a7a19d1
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: b9d88cb954e89cfd6401f674fbbbc901ac634982
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49236362"
---
# <a name="visual-c-enumerations-in-class-designer"></a>Wyliczenia Visual C++ w Projektancie klas
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Projektant klas obsługuje C++ `enum` i zakresami `enum class` typów. Poniżej znajduje się przykład:  
  
```  
enum CardSuit {  
   Diamonds = 1,  
   Hearts = 2,  
   Clubs = 3,  
   Spades = 4  
};  
  
// or...  
enum class CardSuit {  
   Diamonds = 1,  
   Hearts = 2,  
   Clubs = 3,  
   Spades = 4  
};  
  
```  
  
 Kształt wyliczenia C++ na diagramie klasy wygląda i działa jak kształt struktury, chyba że czyta etykietę **wyliczenia** lub **Enum class**, jest różowy, a nie niebieski i ma kolorowe obramowanie na lewym i górnym marginesy. Zarówno wyliczenia kształtów, jak i struktury mają ostre rogi.  
  
 Aby uzyskać więcej informacji o korzystaniu z `enum` typu, zobacz [wyliczenia](http://msdn.microsoft.com/library/081829db-5dca-411e-a53c-bffef315bcb3).  
  
## <a name="see-also"></a>Zobacz też  
 [Praca z kodem Visual C++ (Projektant klas)](../ide/working-with-visual-cpp-code-class-designer.md)   
 [Wyliczenia](http://msdn.microsoft.com/library/081829db-5dca-411e-a53c-bffef315bcb3)



