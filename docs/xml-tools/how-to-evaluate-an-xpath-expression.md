---
title: "Porady: oceny wyrażenia XPath | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 159ba4ef-75e4-4ac8-80dc-e064e0bec345
caps.latest.revision: "2"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: d549afb96465590a21e516f649d860f23f4056f3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-evaluate-an-xpath-expression"></a>Porady: oceny wyrażenia XPath
Można obliczyć wyrażenia XPath z **QuickWatch** okno dialogowe. Wyrażenie XPath musi być prawidłowa zgodnie z zaleceniem W3C XPath 1.0. Bieżącego kontekstu XSLT — to znaczy `self::node()` w węźle **zmiennych lokalnych** okna — udostępnia kontekst oceny dla wyrażenia XPath.  
  
 Na poniższej liście opisano, jakie funkcje są obsługiwane podczas obliczania wyrażenia XPath:  
  
-   Obsługiwane są wbudowane funkcje XPath.  
  
-   Funkcje wbudowane XSLT nie są obsługiwane.  
  
-   Funkcje zdefiniowane przez użytkownika nie są obsługiwane.  
  
> [!NOTE]
>  W poniższej procedurze użyto pliki belowAvg.xsl i books.xml z [wskazówki: debugowanie arkusz stylów XSLT](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md) tematu.  
  
### <a name="to-evaluate-an-xpath-expression"></a>Można oszacować wyrażenia XPath  
  
1.  Wstaw punkt przerwania w `xsl:if` tag początkowy.  
  
2.  Kliknij przycisk **debugowania XSL** przycisk na pasku narzędzi edytora XML.  
  
     Debuger uruchamia i dzieli na `xsl:if` tagu.  
  
3.  Kliknij prawym przyciskiem myszy i wybierz **QuickWatch**.  
  
     **QuickWatch** zostanie wyświetlone okno dialogowe.  
  
4.  Wprowadź `./price/text()` w **wyrażenie** pole **QuickWatch** okno dialogowe i kliknij przycisk **obliczyć ponownie**.  
  
     Cena bieżącego węzła książki pojawia się w **wartość** pole.  
  
5.  Zmień wyrażenie XPath wskazujące `./price/text() < $bookAverage` i kliknij przycisk **obliczyć ponownie**.  
  
     **Wartość** pole pokazuje, że wyrażenie XPath zwraca `true`.  
  
## <a name="see-also"></a>Zobacz też  
 [Profilowanie XSLT](../xml-tools/debugging-xslt.md)