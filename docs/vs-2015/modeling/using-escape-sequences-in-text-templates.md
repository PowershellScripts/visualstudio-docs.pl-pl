---
title: Korzystanie z sekwencji unikowych w szablonach tekstowych | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- text templates, escape sequences
ms.assetid: 36fff542-2f42-460f-a2d5-03fc76817f3b
caps.latest.revision: 31
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: be273c8cf69094a640ea7210bdbdc50005841a49
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296546"
---
# <a name="using-escape-sequences-in-text-templates"></a>Korzystanie z sekwencji unikowych w szablonach tekstowych
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Można użyć sekwencji ucieczki w szablonach tekstowych, które mają być Generowanie tagi szablonu tekstu i (w kodzie języka C# tylko) do anulowania, znaki kontrolne i znaki cudzysłowu.  
  
 Aby wydrukować znaczników otwierających i zamykających w bloku standardowy kod do pliku wyjściowego, ucieczki tagów w następujący sposób:  
  
```  
\<# ... \#>  
```  
  
 Możesz tworzyć taki sam jak inne tekstu szablonu dyrektywy i kod bloku tagi.  
  
 Blok tekstu zawiera ciągi używany jako znak ucieczki znaczniki szablonu tekstu, może użyć poniższej sekwencji ucieczki:  
  
-   Jeśli tag szablonu tekstu jest poprzedzony parzystą liczbą ucieczki (\\) znaków szablonu analizatora będzie połowę znaki ucieczki a sekwencja jako tag szablonu tekstu. Na przykład, jeśli istnieją cztery znaki ucieczki w szablonie tekstowym, nastąpi dwa "\\" znaków w wygenerowanym pliku.  
  
-   Jeśli tag szablonu tekstu jest poprzedzony nieparzystą liczbę ucieczki (\\) znaki, analizator składni szablonu będzie zawierać połowę "\\" znaków oraz samego znacznika (\<# lub #>). Tag nie jest uważany za tag szablonu tekstu.  
  
-   Jeśli znaku ucieczki (\\) znak pojawia się gdziekolwiek w dowolnej kolejności niż gdzie specjalne znaków kontrolnych lub oferty (w języku C# tylko), znaku będą dane wyjściowe bezpośrednio.  
  
## <a name="see-also"></a>Zobacz też  
 [Instrukcje: Generowanie szablonów z szablonów przy użyciu sekwencji ucieczki](../modeling/how-to-generate-templates-from-templates-by-using-escape-sequences.md)



