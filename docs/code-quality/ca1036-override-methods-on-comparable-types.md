---
title: "CA1036: Przesłaniaj metody na typach porównywalnych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1036
- OverrideMethodsOnComparableTypes
helpviewer_keywords:
- OverrideMethodsOnComparableTypes
- CA1036
ms.assetid: 2329f844-4cb8-426d-bee2-cd065d1346d0
caps.latest.revision: "21"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: d07e63363542a9bf5a1dd756026183349659abe1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1036-override-methods-on-comparable-types"></a>CA1036: Przesłaniaj metody na typach porównywalnych
|||  
|-|-|  
|TypeName|OverrideMethodsOnComparableTypes|  
|CheckId|CA1036|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Implementuje typu publiczne lub chronione <xref:System.IComparable?displayProperty=fullName> interfejsu i nie powoduje zastąpienia <xref:System.Object.Equals%2A?displayProperty=fullName> lub nie przeciążać operatora specyficzny dla języka pod kątem równości, nierówności, mniejsze lub większe. Reguła nie Zgłoś naruszenie, jeśli typ dziedziczy implementacji interfejsu.  
  
## <a name="rule-description"></a>Opis reguły  
 Typy definiujące kolejności niestandardowej implementować <xref:System.IComparable> interfejsu. <xref:System.IComparable.CompareTo%2A> Metoda zwraca wartość wskazującą kolejność sortowania poprawne dwa wystąpienia tego typu. Ta zasada identyfikuje typy porządek sortowania; oznacza to, że znaczenie zwykłej równości i nierówności, mniejsza i większa niż nie mają zastosowania. Gdy zapewniać implementację elementu <xref:System.IComparable>, zazwyczaj należy również przesłonić <xref:System.Object.Equals%2A> tak, aby zwraca wartości, które są zgodne z <xref:System.IComparable.CompareTo%2A>. Jeśli można zastąpić <xref:System.Object.Equals%2A> z kodowaniem są w języku, który obsługuje przeciążenia operatorów, należy również podać operatory, które są zgodne z <xref:System.Object.Equals%2A>.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, należy zastąpić <xref:System.Object.Equals%2A>. Jeśli język programowania obsługuje przeciążania operatorów, należy podać następujące operatory:  
  
-   op_Equality  
  
-   op_Inequality  
  
-   op_LessThan  
  
-   op_GreaterThan  
  
 W języku C#, tokeny, które są używane do reprezentowania tych operatorów są następujące: ==,! =, \<, a >.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest bezpieczne pominąć ostrzeżenie od tej reguły, jeśli naruszenie przyczyną jest brak operatory i języka programowania nie obsługuje operatora przeładowanie, jak w przypadku programu Visual Basic .NET. Jest również bezpiecznie Pomiń ostrzeżenie związane z tą regułą, gdy generowane na operatory równości innych niż op_Equality, jeśli użytkownik stwierdzi, że implementacja operatorów nie ma sensu w kontekście Twojej aplikacji. Jednak należy zawsze za pośrednictwem op_Equality i == — operator Jeśli przesłania metody Object.Equals.  
  
## <a name="example"></a>Przykład  
 Poniżej przedstawiono przykład zawierający typu, który implementuje poprawnie <xref:System.IComparable>. Komentarze w kodzie zidentyfikować metody, które spełniają różne zasady, które są powiązane z <xref:System.Object.Equals%2A> i <xref:System.IComparable> interfejsu.  
  
 [!code-csharp[FxCop.Design.IComparable#1](../code-quality/codesnippet/CSharp/ca1036-override-methods-on-comparable-types_1.cs)]  
  
## <a name="example"></a>Przykład  
 Następującej aplikacji testów zachowanie <xref:System.IComparable> implementację, która została przedstawiona wcześniej.  
  
 [!code-csharp[FxCop.Design.TestIComparable#1](../code-quality/codesnippet/CSharp/ca1036-override-methods-on-comparable-types_2.cs)]  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.IComparable?displayProperty=fullName>   
 <xref:System.Object.Equals%2A?displayProperty=fullName>   
 [Operatory porównania](/dotnet/standard/design-guidelines/equality-operators)