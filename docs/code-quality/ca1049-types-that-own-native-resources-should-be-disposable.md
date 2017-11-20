---
title: "CA1049: Typy, które posiadają natywne zasoby powinny być usuwalne | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1049
- TypesThatOwnNativeResourcesShouldBeDisposable
helpviewer_keywords:
- TypesThatOwnNativeResourcesShouldBeDisposable
- CA1049
ms.assetid: 084e587d-0e45-4092-b767-49eed30d6a35
caps.latest.revision: "17"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: ebcb3325cfefdfeeb95b30477c4b266a70f40eb0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1049-types-that-own-native-resources-should-be-disposable"></a>CA1049: Typy, które posiadają natywne zasoby powinny być usuwalne
|||  
|-|-|  
|TypeName|TypesThatOwnNativeResourcesShouldBeDisposable|  
|CheckId|CA1049|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Bez podziału|  
  
## <a name="cause"></a>Przyczyna  
 Odwołuje się do typu <xref:System.IntPtr?displayProperty=fullName> pola <xref:System.UIntPtr?displayProperty=fullName> pola lub <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName> pól, ale nie implementuje <xref:System.IDisposable?displayProperty=fullName>.  
  
## <a name="rule-description"></a>Opis reguły  
 Ta zasada przy założeniu, że <xref:System.IntPtr>, <xref:System.UIntPtr>, i <xref:System.Runtime.InteropServices.HandleRef> pól Zapisz wskaźniki do niezarządzanych zasobów. Typy, które alokują niezarządzane zasoby, powinny implementować <xref:System.IDisposable> aby umożliwić wywołującym zwolnienie tych zasobów na żądanie i skrócić okres istnienia obiektów, które zawierają zasoby.  
  
 Wzorzec projektowy zalecane, aby wyczyścić zasoby niezarządzane jest zapewnienie niejawnych i jawnych oznacza aby zwolnić zasoby przy użyciu <xref:System.Object.Finalize%2A?displayProperty=fullName> — metoda i <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> metody odpowiednio. Wywołania modułu zbierającego elementy bezużyteczne <xref:System.Object.Finalize%2A> metody obiektu w nieokreślonym czasie po obiektu jest określane przestaną być dostępne. Po <xref:System.Object.Finalize%2A> jest wywoływana, dodatkowe wyrzucanie elementów bezużytecznych jest wymagany do zwolnienia obiektu. <xref:System.IDisposable.Dispose%2A> Metoda pozwala obiekt wywołujący, aby jawnie zwolnić zasoby na żądanie, wcześniej niż zasoby będą zwolnione, jeśli od lewej do modułu zbierającego elementy bezużyteczne. Po jego czyści niezarządzane zasoby <xref:System.IDisposable.Dispose%2A> powinny wywoływać <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> metody, aby umożliwić moduł garbage collector pamiętać, że <xref:System.Object.Finalize%2A> nie ma już być wywoływany; to eliminuje potrzebę stosowania dodatkowych wyrzucanie elementów bezużytecznych i skraca okres istnienia obiektu.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby rozwiązać naruszenie tej reguły, zaimplementuj <xref:System.IDisposable>.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest bezpieczne pominąć ostrzeżenie od tej reguły, jeśli typ nie odwołuje się do niezarządzanego zasobu. W przeciwnym razie nie pominąć ostrzeżenie od tej reguły, ponieważ brak implementacji <xref:System.IDisposable> może spowodować, że zasoby niezarządzane stać się niedostępne lub rozłączania.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono typu, który implementuje <xref:System.IDisposable> czyszczenie zasobów niezarządzanych.  
  
 [!code-csharp[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/CSharp/ca1049-types-that-own-native-resources-should-be-disposable_1.cs)]
 [!code-vb[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/VisualBasic/ca1049-types-that-own-native-resources-should-be-disposable_1.vb)]  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA2115: Wywołaj GC. KeepAlive, gdy używasz zasobów natywnych](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)  
  
 [CA1816: Wywołaj GC. Metodę SuppressFinalize poprawnie](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)  
  
 [CA2216: Typy usuwalne powinny deklarować finalizator](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)  
  
 [CA1001: Typy, które posiadają pola usuwalne powinny być usuwalne](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Oczyszczanie zasobów niezarządzanych](/dotnet/standard/garbage-collection/unmanaged)   
 [Wzorzec Dispose](/dotnet/standard/design-guidelines/dispose-pattern)