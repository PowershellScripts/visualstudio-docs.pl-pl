---
title: "CA2215: Metody Dispose powinny wywoływać metodę dispose klasy podstawowej | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA2215
- DisposeMethodsShouldCallBaseClassDispose
- Dispose methods should call base class dispose
helpviewer_keywords:
- DisposeMethodsShouldCallBaseClassDispose
- CA2215
ms.assetid: c772e7a6-a87e-425c-a70e-912664ae9042
caps.latest.revision: "16"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 0659b9ec82353e3c658f1ba89f07fad197dd8670
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2215-dispose-methods-should-call-base-class-dispose"></a>CA2215: Metody Dispose powinny wywoływać operację usuwania klasy podstawowej
|||  
|-|-|  
|TypeName|DisposeMethodsShouldCallBaseClassDispose|  
|CheckId|CA2215|  
|Kategoria|Microsoft.Usage|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Typ, który implementuje <xref:System.IDisposable?displayProperty=fullName> dziedziczy po typie, który też implementuje <xref:System.IDisposable>. <xref:System.IDisposable.Dispose%2A> Nie wywołuje metody typu dziedziczących <xref:System.IDisposable.Dispose%2A> metody typu nadrzędnego.  
  
## <a name="rule-description"></a>Opis reguły  
 Jeśli typ dziedziczy z typu możliwego do likwidacji, musi wywoływać <xref:System.IDisposable.Dispose%2A> metody typu podstawowego z wewnątrz własnego <xref:System.IDisposable.Dispose%2A> metody. Wywołanie metody typu podstawowego Dispose zapewnia zwolnienie wszystkich zasobów tworzone przez typ podstawowy.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby rozwiązać naruszenie tej reguły, należy wywołać `base`.<xref:System.IDisposable.Dispose%2A> w Twojej <xref:System.IDisposable.Dispose%2A> metody.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Można bezpiecznie pominąć ostrzeżenie od tej reguły, jeśli wywołanie `base`.<xref:System.IDisposable.Dispose%2A> występuje na poziomie wywoływania głębiej niż sprawdza reguły.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono typu `TypeA` implementującej <xref:System.IDisposable>.  
  
 [!code-csharp[FxCop.Usage.IDisposablePattern#1](../code-quality/codesnippet/CSharp/ca2215-dispose-methods-should-call-base-class-dispose_1.cs)]  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono typu `TypeB` który dziedziczy z typu `TypeA` i prawidłowo wywołuje jego <xref:System.IDisposable.Dispose%2A> metody.  
  
 [!code-vb[FxCop.Usage.IDisposableBaseCalled#1](../code-quality/codesnippet/VisualBasic/ca2215-dispose-methods-should-call-base-class-dispose_2.vb)]  
  
## <a name="see-also"></a>Zobacz też  
 <xref:System.IDisposable?displayProperty=fullName>   
 [Wzorzec Dispose](/dotnet/standard/design-guidelines/dispose-pattern)