---
title: "CA2227: Właściwości kolekcji powinny być tylko do odczytu | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA2227
- CollectionPropertiesShouldBeReadOnly
helpviewer_keywords:
- CA2227
- CollectionPropertiesShouldBeReadOnly
ms.assetid: 26967aaf-6fbe-438a-b4d3-ac579b5dc0f9
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: df23ab2259bc8042b9a9782ff9f7a15ac349a1c6
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2227-collection-properties-should-be-read-only"></a>CA2227: Właściwości kolekcji powinny być tylko do odczytu
|||  
|-|-|  
|TypeName|CollectionPropertiesShouldBeReadOnly|  
|CheckId|CA2227|  
|Kategoria|Microsoft.Usage|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Widoczne na zewnątrz właściwości z możliwością zapisu jest typu, który implementuje <xref:System.Collections.ICollection?displayProperty=fullName>. Tablice, indeksatory (właściwości o nazwie "Item") i zestawów uprawnień są ignorowane przez regułę.  
  
## <a name="rule-description"></a>Opis reguły  
 Właściwości kolekcji zapisywalny umożliwia użytkownikowi Zamień kolekcji całkowicie innej kolekcji. Właściwość tylko do odczytu uniemożliwia zastępowanie kolekcji, ale nadal umożliwia ustawienie poszczególnych członków. Jeśli celem jest zastąpienie kolekcji, wzorzec projektowy preferowany jest uwzględnienie metodę, aby usunąć wszystkie elementy z kolekcji i metodę ponownie wypełnić kolekcji. Zobacz <xref:System.Collections.ArrayList.Clear%2A> i <xref:System.Collections.ArrayList.AddRange%2A> metody <xref:System.Collections.ArrayList?displayProperty=fullName> klasy przykład tego wzorca.  
  
 Zarówno pliku binarnego, jak i serializacji XML obsługuje właściwości tylko do odczytu, które są kolekcjami. <xref:System.Xml.Serialization.XmlSerializer?displayProperty=fullName> Klasa ma określonych wymagań dotyczących typów, które implementują <xref:System.Collections.ICollection> i <xref:System.Collections.IEnumerable?displayProperty=fullName> aby podlegać serializacji.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby rozwiązać naruszenie tej reguły, skonfigurować właściwość tylko do odczytu, a następnie Jeśli projekt wymaga, Dodaj metody, aby usunąć i ponownie wypełnić kolekcji.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżeń dla tej reguły.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje typ z właściwością zapisywalny kolekcji i pokazuje, jak kolekcji można zastąpić bezpośrednio. Ponadto preferowany sposób zastępowanie właściwości kolekcji tylko do odczytu za pomocą `Clear` i `AddRange` metody jest wyświetlany.  
  
 [!code-csharp[FxCop.Usage.PropertiesReturningCollections#1](../code-quality/codesnippet/CSharp/ca2227-collection-properties-should-be-read-only_1.cs)]
 [!code-vb[FxCop.Usage.PropertiesReturningCollections#1](../code-quality/codesnippet/VisualBasic/ca2227-collection-properties-should-be-read-only_1.vb)]
 [!code-cpp[FxCop.Usage.PropertiesReturningCollections#1](../code-quality/codesnippet/CPP/ca2227-collection-properties-should-be-read-only_1.cpp)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1819: Właściwości nie powinny zwracać tablic](../code-quality/ca1819-properties-should-not-return-arrays.md)