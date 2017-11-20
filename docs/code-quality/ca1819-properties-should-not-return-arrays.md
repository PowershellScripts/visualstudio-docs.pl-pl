---
title: "CA1819: Właściwości nie powinny zwracać tablic | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- PropertiesShouldNotReturnArrays
- CA1819
helpviewer_keywords:
- PropertiesShouldNotReturnArrays
- CA1819
ms.assetid: 85fcf312-57f8-438a-8b10-34441fe0bdeb
caps.latest.revision: "22"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2bd2aae360789646c78fa6b292b1ad97490fc2da
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1819-properties-should-not-return-arrays"></a>CA1819: Właściwości nie powinny zwracać tablic
|||  
|-|-|  
|TypeName|PropertiesShouldNotReturnArrays|  
|CheckId|CA1819|  
|Kategoria|Microsoft.Performance|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Właściwość typu publicznego public lub protected zwraca tablicę.  
  
## <a name="rule-description"></a>Opis reguły  
 Tablice zwrócony przez właściwości nie są zabezpieczony przed zapisem, nawet jeśli właściwość jest tylko do odczytu. Aby zachować tablicę odporną na manipulacje, właściwość musi zwracać kopię tablicy. Zwykle użytkownicy nie rozumieją, jakie niekorzystne następstwa dla wydajności ma wywołanie takiej właściwości. W szczególności mogą użyć właściwości jako właściwość indeksowana.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, ustalić właściwość metodę lub zmień wartość właściwości zwrócić kolekcję.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Atrybuty może zawierać właściwości zwracające tablice, ale nie może zawierać właściwości, które zwracają kolekcje. Można pominąć, ostrzeżenie, że jest wywoływane dla właściwości atrybutu, która jest pochodną <xref:System.Attribute> klasy. W przeciwnym razie nie Pomijaj ostrzeżenia od tej reguły.  
  
## <a name="example-violation"></a>Przykład naruszenie  
  
### <a name="description"></a>Opis  
 W poniższym przykładzie przedstawiono właściwości, która narusza tę regułę.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Performance.PropertyArrayViolation#1](../code-quality/codesnippet/CSharp/ca1819-properties-should-not-return-arrays_1.cs)]
 [!code-vb[FxCop.Performance.PropertyArrayViolation#1](../code-quality/codesnippet/VisualBasic/ca1819-properties-should-not-return-arrays_1.vb)]  
  
### <a name="comments"></a>Komentarze  
 Aby naprawić naruszenie tej reguły, ustalić właściwość metodę lub zmień wartość właściwości zwrócić kolekcję zamiast tablicy.  
  
## <a name="change-the-property-to-a-method-example"></a>Zmień wartość właściwości, na przykład — metoda  
  
### <a name="description"></a>Opis  
 Poniższy przykład poprawia naruszenie, zmieniając właściwość do metody.  
  
### <a name="code"></a>Kod  
 [!code-vb[FxCop.Performance.PropertyArrayFixedMethod#1](../code-quality/codesnippet/VisualBasic/ca1819-properties-should-not-return-arrays_2.vb)]
 [!code-csharp[FxCop.Performance.PropertyArrayFixedMethod#1](../code-quality/codesnippet/CSharp/ca1819-properties-should-not-return-arrays_2.cs)]  
  
## <a name="return-a-collection-example"></a>Zwraca przykład kolekcji  
  
### <a name="description"></a>Opis  
 Poniższy przykład poprawia naruszenie, zmieniając właściwość do zwrócenia  
  
 <xref:System.Collections.ObjectModel.ReadOnlyCollection%601?displayProperty=fullName>.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Performance.PropertyArrayFixedCollection#1](../code-quality/codesnippet/CSharp/ca1819-properties-should-not-return-arrays_3.cs)]
 [!code-vb[FxCop.Performance.PropertyArrayFixedCollection#1](../code-quality/codesnippet/VisualBasic/ca1819-properties-should-not-return-arrays_3.vb)]  
  
## <a name="allowing-users-to-modify-a-property"></a>Zezwalanie użytkownikom na modyfikowanie właściwości  
  
### <a name="description"></a>Opis  
 Możesz zezwolić konsumenta klasy zmodyfikować właściwości. W poniższym przykładzie przedstawiono właściwości odczytu/zapisu, która narusza tę regułę.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Performance.PropertyModifyViolation#1](../code-quality/codesnippet/CSharp/ca1819-properties-should-not-return-arrays_4.cs)]
 [!code-vb[FxCop.Performance.PropertyModifyViolation#1](../code-quality/codesnippet/VisualBasic/ca1819-properties-should-not-return-arrays_4.vb)]  
  
### <a name="comments"></a>Komentarze  
 Poniższy przykład poprawia naruszenie, zmieniając właściwość do zwrócenia <xref:System.Collections.ObjectModel.Collection%601?displayProperty=fullName>.  
  
### <a name="code"></a>Kod  
 [!code-vb[FxCop.Performance.PropertyModifyFixed#1](../code-quality/codesnippet/VisualBasic/ca1819-properties-should-not-return-arrays_5.vb)]
 [!code-csharp[FxCop.Performance.PropertyModifyFixed#1](../code-quality/codesnippet/CSharp/ca1819-properties-should-not-return-arrays_5.cs)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1024: Używaj właściwości wszędzie, gdzie jest to odpowiednie](../code-quality/ca1024-use-properties-where-appropriate.md)