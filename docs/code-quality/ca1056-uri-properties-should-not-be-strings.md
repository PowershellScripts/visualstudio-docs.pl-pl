---
title: "CA1056: Właściwości identyfikatora URI nie powinny być ciągami | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- UriPropertiesShouldNotBeStrings
- CA1056
helpviewer_keywords:
- UriPropertiesShouldNotBeStrings
- CA1056
ms.assetid: fdc99d29-0904-4a65-baa8-4f76833c953e
caps.latest.revision: "12"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 506421ab93cb54c11e1fdfb02c948e4cc8b23d2e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1056-uri-properties-should-not-be-strings"></a>CA1056: Właściwości identyfikatora URI nie powinny być ciągami
|||  
|-|-|  
|TypeName|UriPropertiesShouldNotBeStrings|  
|CheckId|CA1056|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Typ deklaruje właściwości ciągu, których nazwa zawiera "uri", "Identyfikator Uri", "urn", "Urn", "url" lub "Url".  
  
## <a name="rule-description"></a>Opis reguły  
 Ta zasada dzieli nazwę właściwości na tokeny na podstawie Konwencji Pascal wielkość liter i sprawdza, czy każdy token jest równa "uri", "Identyfikator Uri", "urn", "Urn", "url" lub "Url". Jeśli istnieje dopasowanie, reguła przyjęto założenie, że właściwość reprezentuje identyfikator uniform resource identifier (URI). Reprezentacja ciągu identyfikatora URI jest podatna na analizowanie i kodowanie błędów i może prowadzić do powstawania luk w zabezpieczeniach. <xref:System.Uri?displayProperty=fullName> Klasa udostępnia tych usług w sposób bezpieczny i bezpieczne.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, zmień wartość właściwości do <xref:System.Uri> typu.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest bezpieczne pominąć ostrzeżenie od tej reguły, jeśli właściwość nie reprezentuje identyfikator URI.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono typu `ErrorProne`, który narusza tę regułę, a typem, `SaferWay`, odpowiadającej reguły.  
  
 [!code-csharp[FxCop.Design.UriNotString#1](../code-quality/codesnippet/CSharp/ca1056-uri-properties-should-not-be-strings_1.cs)]
 [!code-vb[FxCop.Design.UriNotString#1](../code-quality/codesnippet/VisualBasic/ca1056-uri-properties-should-not-be-strings_1.vb)]
 [!code-cpp[FxCop.Design.UriNotString#1](../code-quality/codesnippet/CPP/ca1056-uri-properties-should-not-be-strings_1.cpp)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1054: Parametry identyfikatora URI nie powinny być ciągami](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)  
  
 [CA1055: Zwracane identyfikatora URI wartości nie powinny być ciągami](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)  
  
 [CA2234: Przekaż obiekty System.Uri zamiast ciągów](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)  
  
 [CA1057: Ciąg URI wywołują przeciążenia System.Uri](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)