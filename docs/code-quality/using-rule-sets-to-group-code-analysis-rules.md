---
title: "Korzystanie z zestawów reguł do grupowania reguł analizy kodu | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.codeanalysis.rulesets.learnmore
helpviewer_keywords: code analysis, rule sets
ms.assetid: ed0f3a2a-1516-42e2-92de-b8986dc75d42
caps.latest.revision: "36"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 44d64b7371f1b27afaa7796dc42d4b7864d20819
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="using-rule-sets-to-group-code-analysis-rules"></a>Korzystanie z zestawów reguł do grupowania reguł analizy kodu
Podczas konfigurowania analizy kodu w [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)], [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)], lub [!INCLUDE[vsPro](../code-quality/includes/vspro_md.md)], można wybrać z listy wbudowanych Microsoft *zestawów reguł*. Zestaw reguł jest logicznym grupowaniem reguł analizy kodu, które identyfikują docelowe problemy i określone warunki. Na przykład można zastosować zestaw reguł przeznaczony do Zeskanuj kod dla publicznie dostępnych interfejsach API, lub możesz zastosować zestaw reguł, który zawiera tylko minimalny zbiór zalecanych reguł. Można także zastosować dla zestawu reguł, który zawiera wszystkie reguły.  
  
 Można dostosować zestaw przez dodanie lub usunięcie zasady lub zmieniając zasady pojawią się w reguł **listy błędów** okno jako ostrzeżenia i błędy. Dostosowane zestawy reguł mogą spełnić potrzeby konkretnego środowiska do tworzenia oprogramowania. Po dostosowaniu zestawu reguł strona zestawu reguł dostarcza narzędzia do wyszukiwania i filtrowania pomocne w przetwarzaniu.  
  
## <a name="common-tasks"></a>Typowe zadania  
  
|Zadanie|Zawartość pokrewna|  
|----------|---------------------|  
|**Pobierz przećwiczenia:** użyj narzędzi analizy kodu, aby określić niestandardową regułę ustawioną na znajdowanie i rozwiązywanie problemów w prostej aplikacji .NET Framework.|-   [Wskazówki: Konfigurowanie i używanie niestandardowego zestawu reguł](../code-quality/walkthrough-configuring-and-using-a-custom-rule-set.md)|  
|**Konfigurowanie analizy kodu dla projektu:** wybrać istniejącą regułę dla projektu, witryny sieci Web lub rozwiązania.|-   [Porady: Konfigurowanie analizy kodu dla projektu zarządzanego kodu](../code-quality/how-to-configure-code-analysis-for-a-managed-code-project.md)<br />-   [Korzystanie z zestawów reguł do określania reguł C++ do uruchomienia](../code-quality/using-rule-sets-to-specify-the-cpp-rules-to-run.md)<br />-   [Porady: Konfigurowanie analizy kodu dla aplikacji sieci Web ASP.NET](../code-quality/how-to-configure-code-analysis-for-an-aspnet-web-application.md)<br />-   [Porady: określanie zestawów reguł dla wielu projektów w rozwiązaniu](../code-quality/how-to-specify-managed-code-rule-sets-for-multiple-projects-in-a-solution.md)|  
|**Dostosowywanie zestawu reguł:** Określ reguły do zastosowania do projektu.|-   [Tworzenie niestandardowych zestawów reguł](../code-quality/creating-custom-code-analysis-rule-sets.md)|  
|**Zrozumienie zestawy wbudowanych reguł:** wyświetlić reguły analizy kodu, które tworzą zestawy wbudowanych reguł.|-   [Odwołanie zestawu reguł analizy kodu](../code-quality/code-analysis-rule-set-reference.md)|  
|**Integracja z Team Foundation Server analizy kodu:** [!INCLUDE[esprtfs](../code-quality/includes/esprtfs_md.md)] zaewidencjonowania zasady umożliwiają zespołom projektowanie upewnij się, że wszystkie zaewidencjonowania kodu spełniają wspólny zbiór standardów analizy kodu.|-   [Porady: synchronizowanie zestawu reguł projektu kodu z zasadami ewidencjonowania projektu zespołowego](../code-quality/how-to-synchronize-code-project-rule-sets-with-team-project-check-in-policy.md)|