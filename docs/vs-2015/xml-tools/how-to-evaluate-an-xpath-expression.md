---
title: 'Instrukcje: Ocena wyrażenia XPath | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 159ba4ef-75e4-4ac8-80dc-e064e0bec345
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 05758034c0228f0efd7fb3ae63bd3b7e0d5e3095
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49210434"
---
# <a name="how-to-evaluate-an-xpath-expression"></a>Instrukcje: Ocena wyrażenia XPath
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Można obliczyć wyrażenia XPath z **QuickWatch** okno dialogowe. Wyrażenie XPath muszą być prawidłowe zgodnie z zaleceniem W3C XPath 1.0. Bieżący kontekst w XSLT — oznacza to, `self::node()` w węźle **lokalne** okna — zapewnia kontekstu oceny wyrażenia XPath.  
  
 Na poniższej liście opisano, jakie funkcje są obsługiwane podczas obliczania wyrażenia XPath:  
  
-   Wbudowane funkcje XPath są obsługiwane.  
  
-   Wbudowane funkcje XSLT nie są obsługiwane.  
  
-   Funkcje zdefiniowane przez użytkownika nie są obsługiwane.  
  
> [!NOTE]
>  W poniższej procedurze użyto belowAvg.xsl i books.xml pliki z [wskazówki: debugowanie arkusza stylów XSLT](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md) tematu.  
  
### <a name="to-evaluate-an-xpath-expression"></a>Aby szacować wyrażenia XPath  
  
1.  Wstaw punkt przerwania w `xsl:if` taga otwierającego.  
  
2.  Kliknij przycisk **debugowania XSL** na listwie narzędziowej edytora XML.  
  
     Debuger rozpoczyna się i przerywa na `xsl:if` tagu.  
  
3.  Kliknij prawym przyciskiem myszy i wybierz **QuickWatch**.  
  
     **QuickWatch** zostanie wyświetlone okno dialogowe.  
  
4.  Wprowadź `./price/text()` w **wyrażenie** pole **QuickWatch** dialogowym i kliknij przycisk **to ponowne ocenienie**.  
  
     Cena bieżącego węzła książki, który pojawia się w **wartość** pole.  
  
5.  Zmień wyrażenie XPath `./price/text() < $bookAverage` i kliknij przycisk **to ponowne ocenienie**.  
  
     **Wartość** pole pokazuje, że wyrażenie XPath daje w wyniku `true`.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie kodu XSLT](../xml-tools/debugging-xslt.md)

