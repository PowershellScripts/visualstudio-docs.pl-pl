---
title: Rozwiązywanie problemów z analizą kodu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 61c7e44d-2780-4df5-9bcb-49e40c1152fc
caps.latest.revision: 7
author: erickson-doug
ms.author: gewarren
manager: douge
ms.openlocfilehash: 1b21666094d2a13054be49980028afcc7a7e39a3
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49229791"
---
# <a name="troubleshooting-code-analysis-issues"></a>Rozwiązywanie problemów związanych z analizą kodu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ten temat zawiera informacje dotyczące rozwiązywania problemów dla następujących problemów z analizą kodu programu Visual Studio.  
  
-   [Zmiany w Visual Studio 2010 reguły zestawu są nie zostaną uwzględnione w poprzednich wersjach programu Visual Studio](#ChildRuleSetChangesInPreviousVersions)  
  
##  <a name="ChildRuleSetChangesInPreviousVersions"></a> Zmiany w Visual Studio 2010 reguły zestawu są nie zostaną uwzględnione w poprzednich wersjach programu Visual Studio  
 Po utworzeniu zestaw reguł w [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] zawierającą podrzędny zestaw reguł, zmiany do zestawu reguł podrzędne mogą nie zostać zastosowane w przebiegi analizy kodu na komputerach, które korzystają z wcześniejszej wersji programu Visual Studio. Aby rozwiązać ten problem, możesz wymusić nadpisania zestaw reguł nadrzędnego, który jest zestaw reguł, który zawiera zestaw reguł podrzędnych.  
  
1.  Otwórz zestaw reguł nadrzędnego, [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)].  
  
2.  Wprowadź zmiany, takie jak dodawanie lub usuwanie reguły, a następnie Zapisz zestaw reguł.  
  
3.  Otwórz zestaw reguł, odwrócić zmiany, a następnie zapisz ponownie zestaw reguł.  
  
## <a name="see-also"></a>Zobacz też  
 [Analiza jakości aplikacji](../code-quality/analyzing-application-quality-by-using-code-analysis-tools.md)   
 [Analiza jakości zarządzanego kodu](../code-quality/analyzing-managed-code-quality-by-using-code-analysis.md)   
 [Korzystanie z zestawów reguł do grupowania reguł analizy kodu](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)



