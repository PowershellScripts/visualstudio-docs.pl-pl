---
title: 'CA1016: Oznacz zestawy atrybutem Assemblyversion | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- MarkAssembliesWithAssemblyVersion
- CA1016
helpviewer_keywords:
- CA1016
- MarkAssembliesWithAssemblyVersion
ms.assetid: 4340aed8-d92b-4cde-a398-cb6963c6da5a
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: cb3cb13484d427bb5389a0ec89573231376efdf8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49811144"
---
# <a name="ca1016-mark-assemblies-with-assemblyversionattribute"></a>CA1016: Oznacz zestawy za pomocą AssemblyVersionAttribute
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkAssembliesWithAssemblyVersion|
|CheckId|CA1016|
|Kategoria|Microsoft.Design|
|Zmiana kluczowa|Bez podziału|

## <a name="cause"></a>Przyczyna
 Zestaw nie ma numeru wersji.

## <a name="rule-description"></a>Opis reguły
 Tożsamość zestawu składa się z następujących informacji:

- Nazwa zestawu

- Numer wersji

- Kultury

- Klucz publiczny (w przypadku zestawów o silnej nazwie).

  [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] Używa numeru wersji, aby jednoznacznie zidentyfikować zestaw i powiązać z typami w zestawach o silnej nazwie. Numer wersji jest używany razem z zasadami wersji i wydawcy. Domyślnie aplikacje są uruchamiane tylko z wersji zestawu, z którego zostały zbudowane.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, Dodaj numer wersji do zestawu przy użyciu <xref:System.Reflection.AssemblyVersionAttribute?displayProperty=fullName> atrybutu. Zobacz poniższy przykład.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły dla zestawów, które są używane przez strony trzecie lub w środowisku produkcyjnym.

## <a name="example"></a>Przykład
 W poniższym przykładzie przedstawiono zestaw, który ma <xref:System.Reflection.AssemblyVersionAttribute> zastosowany.

 [!code-cpp[FxCop.Design.AssembliesVersion#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesVersion/cpp/FxCop.Design.AssembliesVersion.cpp#1)]
 [!code-csharp[FxCop.Design.AssembliesVersion#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesVersion/cs/FxCop.Design.AssembliesVersion.cs#1)]
 [!code-vb[FxCop.Design.AssembliesVersion#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesVersion/vb/FxCop.Design.AssembliesVersion.vb#1)]

## <a name="see-also"></a>Zobacz też
 [Przechowywanie wersji zestawu](http://msdn.microsoft.com/library/775ad4fb-914f-453c-98ef-ce1089b6f903) [porady: Tworzenie zasad wydawcy](http://msdn.microsoft.com/library/8046bc5d-2fa9-4277-8a5e-6dcc96c281d9)



