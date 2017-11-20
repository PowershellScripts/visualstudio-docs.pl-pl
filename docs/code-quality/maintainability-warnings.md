---
title: "Ostrzeżenia dotyczące utrzymania | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.codeanalysis.maintainabilityrules
helpviewer_keywords:
- warnings, maintainability
- managed code analysis warnings, maintainability warnings
- maintainability warnings
ms.assetid: 537e70ca-a88c-49df-bfc7-0ee63bbe4f16
caps.latest.revision: "19"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 88199541fe5d3c4be3f9f1cff6de308d45d0d85a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="maintainability-warnings"></a>Utrzymanie — Ostrzeżenia
Ostrzeżenia dotyczące utrzymania obsługuje konserwacji biblioteki i aplikacji.  
  
## <a name="in-this-section"></a>W tej sekcji  
  
|Reguła|Opis|  
|----------|-----------------|  
|[CA1500: Nazwy zmiennych nie powinny odpowiadać nazwom pól](../code-quality/ca1500-variable-names-should-not-match-field-names.md)|Metody wystąpienia deklaruje parametr lub zmienna lokalna, którego nazwa odpowiada pole wystąpienia typu deklarującego, co prowadzi do błędów.|  
|[CA1501: Unikaj nadmiernego dziedziczenia](../code-quality/ca1501-avoid-excessive-inheritance.md)|Typ jest głęboki na więcej niż cztery poziomy w hierarchii dziedziczenia. Hierarchie typów głęboko zagnieżdżonych mogą być trudne do śledzenia, zrozumienia i utrzymania.|  
|[CA1502: Unikaj nadmiernej złożoności](../code-quality/ca1502-avoid-excessive-complexity.md)|Ta reguła mierzy liczbę liniowo niezależnych ścieżek za pośrednictwem metody, która jest określona przez liczbę i złożoność rozgałęzień warunkowych.|  
|[CA1504: Przegląd mylących nazw pól](../code-quality/ca1504-review-misleading-field-names.md)|Nazwa pola wystąpienia rozpoczyna się od "s_", albo w nazwie statycznego (Shared w [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) pola rozpoczyna się ciągiem "m_".|  
|[CA1505: Unikaj kodu](../code-quality/ca1505-avoid-unmaintainable-code.md)|Typ lub metoda ma niską wartość indeksu konserwacji. Niski indeks konserwacji wskazuje, że typ lub metoda są prawdopodobnie trudne do utrzymania i są dobrymi kandydatami do przeprojektowania.|  
|[CA1506: Unikaj nadmiernego sprzężenia klas](../code-quality/ca1506-avoid-excessive-class-coupling.md)|Ta reguła mierzy sprzęgnięcie klasy przez liczenie unikatowych odwołań typów, które zawiera typ lub metoda.|  
  
## <a name="see-also"></a>Zobacz też  
 [Mierzenie złożoności i łatwości konserwacji zarządzanego kodu](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)