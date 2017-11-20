---
title: "CA2243: Literały ciągu atrybutu powinny być analizowane poprawnie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA2243
- AttributeStringLiteralsShouldParseCorrectly
helpviewer_keywords:
- AttributeStringLiteralsShouldParseCorrectly
- CA2243
ms.assetid: bfadb366-379d-4ee4-b17b-c4a09bf1106b
caps.latest.revision: "10"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 3ec86725873f5724609f411072dab4a4bde9d990
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2243-attribute-string-literals-should-parse-correctly"></a>CA2243: Literały ciągu atrybutu powinny być analizowane poprawnie
|||  
|-|-|  
|TypeName|AttributeStringLiteralsShouldParseCorrectly|  
|CheckId|CA2243|  
|Kategoria|Microsoft.Usage|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Parametr literału ciągu atrybutu nie poprawnie przeanalizować adresu URL, GUID lub wersji.  
  
## <a name="rule-description"></a>Opis reguły  
 Ponieważ atrybuty są uzyskiwane z <xref:System.Attribute?displayProperty=fullName>i w czasie kompilacji są używane atrybuty, tylko wartości stałych można przekazać do ich konstruktorów. Parametry atrybutów reprezentujące musi adresów URL, identyfikatory GUID i wersje nie może być typizowana jako <xref:System.Uri?displayProperty=fullName>, <xref:System.Guid?displayProperty=fullName>, i <xref:System.Version?displayProperty=fullName>, ponieważ te typy nie może być reprezentowany jako stałe. Zamiast tego musi być reprezentowana przez parametry.  
  
 Ponieważ parametr jest typu ciąg, jest możliwe, że parametr niepoprawnie sformatowany można przekazany w czasie kompilacji.  
  
 Ta zasada używa nazewnictwa heurystyki w celu wyszukania parametry, które reprezentują jednolitego identyfikatora zasobów (URI), globalnie unikatowy identyfikator (GUID) lub wersji i sprawdza, czy przekazana wartość jest poprawna.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Zmień ciąg parametru poprawnie sformułowany adres URL, GUID lub wersji.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest bezpieczne pominąć ostrzeżenie od tej reguły, jeśli parametr nie reprezentuje adres URL, GUID lub wersji.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład przedstawia kod dla AssemblyFileVersionAttribute, który narusza tę regułę.  
  
 [!code-csharp[FxCop.Usage.AttributeStringLiteralsShouldParseCorrectly#1](../code-quality/codesnippet/CSharp/ca2243-attribute-string-literals-should-parse-correctly_1.cs)]  
  
 Reguła jest wyzwalana przez następujące czynności:  
  
-   Parametry, które zawierają "version" i nie można przeanalizować System.Version.  
  
-   Parametry, które zawierają "guid" i nie można przeanalizować System.Guid.  
  
-   Parametry, które zawierają "uri", "urn" lub "url" i nie może być analizowana na System.Uri.  
  
## <a name="see-also"></a>Zobacz też  
 [CA1054: Parametry identyfikatora URI nie powinny być ciągami](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)