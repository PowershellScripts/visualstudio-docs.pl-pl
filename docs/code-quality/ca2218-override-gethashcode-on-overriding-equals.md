---
title: "CA2218: Zastąp GetHashCode przy zastępowaniu Equals | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA2218
- OverrideGetHashCodeOnOverridingEquals
helpviewer_keywords:
- OverrideGetHashCodeOnOverridingEquals
- CA2218
ms.assetid: 69b020cd-29e8-45a6-952e-32cf3ce2e21d
caps.latest.revision: "20"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: fa24be65377c563e6118fa99ab2983ee407874b3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2218-override-gethashcode-on-overriding-equals"></a>CA2218: Zastąp GetHashCode przy zastępowaniu Equals
|||  
|-|-|  
|TypeName|OverrideGetHashCodeOnOverridingEquals|  
|CheckId|CA2218|  
|Kategoria|Microsoft.Usage|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Zastępuje typu publicznego <xref:System.Object.Equals%2A?displayProperty=fullName> , ale nie przesłania <xref:System.Object.GetHashCode%2A?displayProperty=fullName>.  
  
## <a name="rule-description"></a>Opis reguły  
 <xref:System.Object.GetHashCode%2A>Zwraca wartość, w oparciu o bieżące wystąpienie, który jest odpowiedni dla algorytmów wyznaczania wartości skrótu i struktury danych, takich jak tablicy skrótów. Dwa obiekty są tego samego typu, które są takie same musi zwracać taki sam skrót, aby zapewnić poprawne działanie wystąpień następujących typów:  
  
-   <xref:System.Collections.Hashtable?displayProperty=fullName>  
  
-   <xref:System.Collections.SortedList?displayProperty=fullName>  
  
-   <xref:System.Collections.Generic.Dictionary%602?displayProperty=fullName>  
  
-   <xref:System.Collections.Generic.SortedDictionary%602?displayProperty=fullName>  
  
-   <xref:System.Collections.Generic.SortedList%602?displayProperty=fullName>  
  
-   <xref:System.Collections.Specialized.HybridDictionary?displayProperty=fullName>  
  
-   <xref:System.Collections.Specialized.ListDictionary?displayProperty=fullName>  
  
-   <xref:System.Collections.Specialized.OrderedDictionary?displayProperty=fullName>  
  
-   Typy implementujące<xref:System.Collections.Generic.IEqualityComparer%601?displayProperty=fullName>  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, zapewniać implementację elementu <xref:System.Object.GetHashCode%2A>. Dla pary obiektów tego samego typu, należy upewnić się, że implementacja zwraca tę samą wartość, jeśli implementacji <xref:System.Object.Equals%2A> zwraca `true` dla pary.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżeń dla tej reguły.  
  
## <a name="class-example"></a>Przykład klasy  
  
### <a name="description"></a>Opis  
 W poniższym przykładzie przedstawiono klasę (typ odwołania), która narusza tę regułę.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Usage.GetHashCodeErrorClass#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_1.cs)]  
  
### <a name="comments"></a>Komentarze  
 Poniższy przykład poprawia naruszenie przez zastąpienie <xref:System.Object.GetHashCode>.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Usage.GetHashCodeFixedClass#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_2.cs)]  
  
## <a name="structure-example"></a>Przykład struktury  
  
### <a name="description"></a>Opis  
 W poniższym przykładzie przedstawiono struktury (typ wartości), który narusza tę regułę.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Usage.GetHashCodeErrorStruct#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_3.cs)]  
  
### <a name="comments"></a>Komentarze  
 Poniższy przykład poprawia naruszenie przez zastąpienie <xref:System.Object.GetHashCode>.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Usage.GetHashCodeFixedStruct#1](../code-quality/codesnippet/CSharp/ca2218-override-gethashcode-on-overriding-equals_4.cs)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1046: Nie przeciążaj operatora równości w typach referencyjnych](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)  
  
 [CA2225: Operator overloads ma nazwanych zastępców](../code-quality/ca2225-operator-overloads-have-named-alternates.md)  
  
 [CA2226: Operatory powinny mieć symetryczne przeciążenia](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)  
  
 [CA2224: Przesłoń metodę equals przeciążając operator equals](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)  
  
 [CA2231: Przeciąż operator equals przy zastępowaniu ValueType.Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.Object.Equals%2A?displayProperty=fullName>   
 <xref:System.Object.GetHashCode%2A?displayProperty=fullName>   
 <xref:System.Collections.Hashtable?displayProperty=fullName>   
 [Operatory porównania](/dotnet/standard/design-guidelines/equality-operators)