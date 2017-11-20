---
title: 'CA1017: Oznacz zestawy atrybutem ComVisibleAttribute | Dokumentacja firmy Microsoft'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1017
- MarkAssembliesWithComVisible
helpviewer_keywords:
- MarkAssembliesWithComVisible
- CA1017
ms.assetid: 4842cb49-8dd8-4e5d-a2d6-ceeaf6c6cf8e
caps.latest.revision: "19"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5e4c76efff009c85f9d607611d92d53cad5d2759
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1017-mark-assemblies-with-comvisibleattribute"></a>CA1017: Oznacz zestawy za pomocą ComVisibleAttribute
|||  
|-|-|  
|TypeName|MarkAssembliesWithComVisible|  
|CheckId|CA1017|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Zestaw nie ma <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> atrybut zastosowany do niego.  
  
## <a name="rule-description"></a>Opis reguły  
 <xref:System.Runtime.InteropServices.ComVisibleAttribute> Atrybut określa, jak klienci COM dostępu do kodu zarządzanego. Zasada dobrego projektowania nakazuje, aby zestawy jawnie wskazywały widoczność COM. Widoczność COM można ustawić dla całego zestawu i następnie przesłonięcia dla poszczególnych typów i członków typu. Jeśli ten atrybut nie jest obecny, zawartość zestawu są widoczne dla klientów modelu COM.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, Dodaj atrybut do zestawu. Jeśli nie chcesz, aby zestawu, które mają być widoczne dla klientów modelu COM, zastosuj atrybut i ustaw dla niego wartość `false`.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżeń dla tej reguły. Zestaw był widoczny, zastosuj atrybut i ustaw dla niego wartość `true`.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono zestawu, który ma <xref:System.Runtime.InteropServices.ComVisibleAttribute> atrybut zastosowany do uniemożliwiają widoczne dla klientów modelu COM.  
  
 [!code-cpp[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/CPP/ca1017-mark-assemblies-with-comvisibleattribute_1.cpp)]
 [!code-vb[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/VisualBasic/ca1017-mark-assemblies-with-comvisibleattribute_1.vb)]
 [!code-csharp[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/CSharp/ca1017-mark-assemblies-with-comvisibleattribute_1.cs)]  
  
## <a name="see-also"></a>Zobacz też  
 [Współdziałanie z kodem niezarządzanym](/dotnet/framework/interop/index)   
 [Kwalifikowanie typów .NET do międzyoperacyjności](/dotnet/framework/interop/qualifying-net-types-for-interoperation)