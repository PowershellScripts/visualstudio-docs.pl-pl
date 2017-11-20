---
title: "CA1028: Pamięć wyliczenia powinna być Int32 | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1028
- EnumStorageShouldBeInt32
helpviewer_keywords:
- EnumStorageShouldBeInt32
- CA1028
ms.assetid: 87160825-9f39-4142-8d7f-a31fe7ac7b84
caps.latest.revision: "19"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: bd0f74a322e136263b6445db2692380dfea2efa3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1028-enum-storage-should-be-int32"></a>CA1028: Pamięć wyliczenia powinna być Int32
|||  
|-|-|  
|TypeName|EnumStorageShouldBeInt32|  
|CheckId|CA1028|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Nie jest typem podstawowym Wyliczenie publiczne <xref:System.Int32?displayProperty=fullName>.  
  
## <a name="rule-description"></a>Opis reguły  
 Wyliczenie to typ wartości, który definiuje zestaw powiązanych, nazwanych stałych. Domyślnie <xref:System.Int32?displayProperty=fullName> — typ danych jest używany do przechowywania wartości stałej. Mimo że można go zmienić typ podstawowy, nie jest konieczne ani zalecana dla większości scenariuszy. Należy pamiętać, że nie są bardziej wydajne istotne jest realizowane za pośrednictwem typu danych, która jest mniejsza niż <xref:System.Int32>. Jeśli nie możesz użyć domyślnego typu danych, należy użyć jednej wspólnej systemu języka (CLS)-zgodne typy całkowite, <xref:System.Byte>, <xref:System.Int16>, <xref:System.Int32>, lub <xref:System.Int64> aby upewnić się, że wszystkie wartości wyliczenia można przedstawić w Zgodne ze specyfikacją CLS języków programowania.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby rozwiązać naruszenie tej reguły, o ile istnieją problemy rozmiaru lub zgodność, należy użyć <xref:System.Int32>. W sytuacjach, gdy <xref:System.Int32> nie jest wystarczająco duży, aby pomieścić wartości, użyj <xref:System.Int64>. Jeśli zgodność z poprzednimi wersjami wymaga na mniejszy typ danych, należy użyć <xref:System.Byte> lub <xref:System.Int16>.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Pomiń ostrzeżenie od tej zasady tylko wtedy, gdy problemy ze zgodnością z poprzednimi wersjami tego wymagają. W aplikacjach brak zgodności z tą regułą zazwyczaj nie powoduje problemów. W bibliotekach, w którym wymagany jest współdziałanie języków, brak zgodności z tą regułą może niekorzystnie wpłynąć na użytkowników.  
  
## <a name="example-of-a-violation"></a>Przykładem naruszenia  
  
### <a name="description"></a>Opis  
 Poniższy przykład przedstawia dwa wyliczenia, które nie korzystają z zalecanych podstawowy typ danych.  
  
### <a name="code"></a>Kod  
 [!code-vb[FxCop.Design.EnumIntegralType#1](../code-quality/codesnippet/VisualBasic/ca1028-enum-storage-should-be-int32_1.vb)]
 [!code-csharp[FxCop.Design.EnumIntegralType#1](../code-quality/codesnippet/CSharp/ca1028-enum-storage-should-be-int32_1.cs)]  
  
## <a name="example-of-how-to-fix"></a>Przykładem do naprawy  
  
### <a name="description"></a>Opis  
 Poniższy przykład poprawki poprzedniej naruszenie, zmieniając typ podstawowy danych do <xref:System.Int32>.  
  
### <a name="code"></a>Kod  
 [!code-csharp[FxCop.Design.EnumIntegralTypeFixed#1](../code-quality/codesnippet/CSharp/ca1028-enum-storage-should-be-int32_2.cs)]
 [!code-vb[FxCop.Design.EnumIntegralTypeFixed#1](../code-quality/codesnippet/VisualBasic/ca1028-enum-storage-should-be-int32_2.vb)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1008: Wyliczenia powinny mieć wartości zerowej](../code-quality/ca1008-enums-should-have-zero-value.md)  
  
 [CA1027: Oznaczaj wyliczenia za pomocą FlagsAttribute](../code-quality/ca1027-mark-enums-with-flagsattribute.md)  
  
 [CA2217: Nie oznaczaj typów wyliczeniowych atrybutem FlagsAttribute](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)  
  
 [CA1700: Nie nadawać wartościom enum oznaczenia "Reserved"](../code-quality/ca1700-do-not-name-enum-values-reserved.md)  
  
 [CA1712: Nie dodawaj prefiksu wartości enum nazwą typu](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.Byte?displayProperty=fullName>   
 <xref:System.Int16?displayProperty=fullName>   
 <xref:System.Int32?displayProperty=fullName>   
 <xref:System.Int64?displayProperty=fullName>