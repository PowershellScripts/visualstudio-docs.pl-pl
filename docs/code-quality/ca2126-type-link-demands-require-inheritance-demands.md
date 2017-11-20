---
title: "CA2126: Typ żądań konsolidacji wymaga żądań dziedziczenia | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA2126
- TypeLinkDemandsRequireInheritanceDemands
helpviewer_keywords:
- CA2126
- TypeLinkDemandsRequireInheritanceDemands
ms.assetid: 07b604e5-5579-4df9-a578-dadd0d8370a7
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 254fd15f97afe69f927bb8a1aae1954105776641
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2126-type-link-demands-require-inheritance-demands"></a>CA2126: Typ żądań konsolidacji wymaga żądań dziedziczenia
|||  
|-|-|  
|TypeName|TypeLinkDemandsRequireInheritanceDemands|  
|CheckId|CA2126|  
|Kategoria|Microsoft.Security|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Publiczny typ niezapieczętowany jest chroniony z żądanie łącza ma metodę możliwym do zastąpienia, a typ ani metoda nie jest chroniony za pomocą żądanie dziedziczenia.  
  
## <a name="rule-description"></a>Opis reguły  
 Linkdemand, metody lub jej typ deklarujący wymaga bezpośredniego obiektu wywołującego metody mają określone uprawnienie. Żądanie dziedziczenia dla metody wymaga Zastępowanie metody mają określone uprawnienie. Żądanie dziedziczenia typu wymaga Klasa pochodna ma określone uprawnienie.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, bezpieczny typ lub metoda o żądanie dziedziczenia dla danego uprawnienia linkdemand.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżeń dla tej reguły.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład przedstawia typu, który narusza zasady.  
  
 [!code-cpp[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/CPP/ca2126-type-link-demands-require-inheritance-demands_1.cpp)]
 [!code-vb[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/VisualBasic/ca2126-type-link-demands-require-inheritance-demands_1.vb)]
 [!code-csharp[FxCop.Security.TypesWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2126-type-link-demands-require-inheritance-demands_1.cs)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [Ca2108: należy Przeglądnąć zabezpieczenia deklaratywne dla typów wartości](../code-quality/ca2108-review-declarative-security-on-value-types.md)  
  
 [CA2112: Typy zabezpieczone nie powinny ujawniać pól](../code-quality/ca2112-secured-types-should-not-expose-fields.md)  
  
 [CA2122: Nie ujawniaj pośrednio metod żądaniami linkdemand](../code-quality/ca2122-do-not-indirectly-expose-methods-with-link-demands.md)  
  
 [CA2123: Zastąpienia powinny być identyczne z bazowym](../code-quality/ca2123-override-link-demands-should-be-identical-to-base.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Wytyczne dotyczące bezpiecznego programowania](/dotnet/standard/security/secure-coding-guidelines)   
 [Żądań dziedziczenia](http://msdn.microsoft.com/en-us/28b9adbb-8f08-4f10-b856-dbf59eb932d9)   
 [Żądania łączy](/dotnet/framework/misc/link-demands)   
 [Wymagania](http://msdn.microsoft.com/en-us/e5283e28-2366-4519-b27d-ef5c1ddc1f48)