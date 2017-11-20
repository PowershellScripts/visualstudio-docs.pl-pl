---
title: "CA1804: Usuń nieużywane zmienne lokalne | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1804
- RemoveUnusedLocals
helpviewer_keywords:
- RemoveUnusedLocals
- CA1804
ms.assetid: cc332e67-6543-4813-bd8a-6f6fc75bf22a
caps.latest.revision: "18"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 9217f3109c6ef03de33e444e723caa585d065efb
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1804-remove-unused-locals"></a>CA1804: Usuń nieużywane zmienne lokalne
|||  
|-|-|  
|TypeName|RemoveUnusedLocals|  
|CheckId|CA1804|  
|Kategoria|Microsoft.Performance|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Metoda deklaruje zmienną lokalną, ale nie używa prawdopodobnie zmiennej z wyjątkiem adresata instrukcji przypisania. Do analizy przez tę regułę muszą zostać skompilowane przetestowany zestawu z informacji o debugowaniu i program skojarzony plik bazy danych (.pdb) muszą być dostępne.  
  
## <a name="rule-description"></a>Opis reguły  
 Nieużywane zmienne lokalne i niepotrzebne przydziały zwiększają rozmiar zestawu i zmniejszają wydajność.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, usuń lub użyć zmiennej lokalnej. Należy pamiętać, że kompilator języka C# który dołączone [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)] Usuwa nieużywane zmienne lokalne podczas `optimize` opcja jest włączona.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Pomiń ostrzeżenie od tej reguły, jeśli zmienna kompilatora wysyłanego. Istnieje również bezpieczne, aby pominąć ostrzeżenie od tej reguły, lub można wyłączyć reguły, jeśli wydajność i konserwacja kodu nie są główne obawy.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie pokazano kilka nieużywane zmienne lokalne.  
  
 [!code-vb[FxCop.Performance.UnusedLocals#1](../code-quality/codesnippet/VisualBasic/ca1804-remove-unused-locals_1.vb)]
 [!code-csharp[FxCop.Performance.UnusedLocals#1](../code-quality/codesnippet/CSharp/ca1804-remove-unused-locals_1.cs)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1809: Unikaj nadmiernego zmiennych lokalnych](../code-quality/ca1809-avoid-excessive-locals.md)  
  
 [CA1811: Unikaj niewywołanego kodu prywatnego](../code-quality/ca1811-avoid-uncalled-private-code.md)  
  
 [CA1812: Unikaj wewnętrznych klas bez wystąpień](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)  
  
 [CA1801: Przejrzyj nieużywane parametry](../code-quality/ca1801-review-unused-parameters.md)