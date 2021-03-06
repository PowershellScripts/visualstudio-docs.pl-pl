---
title: 'CA1049: Typy, które posiadają natywne zasoby powinny być usuwalne'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1049
- TypesThatOwnNativeResourcesShouldBeDisposable
helpviewer_keywords:
- TypesThatOwnNativeResourcesShouldBeDisposable
- CA1049
ms.assetid: 084e587d-0e45-4092-b767-49eed30d6a35
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- cplusplus
ms.openlocfilehash: f9a2eeb032951df86d38075220c14fe98488edef
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2018
ms.locfileid: "45551999"
---
# <a name="ca1049-types-that-own-native-resources-should-be-disposable"></a>CA1049: Typy, które posiadają natywne zasoby powinny być usuwalne

|||
|-|-|
|TypeName|TypesThatOwnNativeResourcesShouldBeDisposable|
|CheckId|CA1049|
|Kategoria|Microsoft.Design|
|Zmiana kluczowa|Bez podziału|

## <a name="cause"></a>Przyczyna

Odwołuje się do typu <xref:System.IntPtr?displayProperty=fullName> pola <xref:System.UIntPtr?displayProperty=fullName> pola lub <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName> pola, ale nie implementuje <xref:System.IDisposable?displayProperty=fullName>.

## <a name="rule-description"></a>Opis reguły

Reguła ta zakłada, że <xref:System.IntPtr>, <xref:System.UIntPtr>, i <xref:System.Runtime.InteropServices.HandleRef> pola Zapisz wskaźniki do niezarządzanych zasobów. Typy, które alokują niezarządzane zasoby, powinny implementować <xref:System.IDisposable> aby umożliwić wywołującym zwolnienie tych zasobów na żądanie i skrócenie czasu istnienia obiektów, które zawierają te zasoby.

Zalecany wzorzec projektowania do wyczyścić niezarządzane zasoby ma na celu dostarczenie ukrytego i oznacza, że jawne zwolnienie tych zasobów za pomocą <xref:System.Object.Finalize%2A?displayProperty=fullName> metody i <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> metody, odpowiednio. Moduł odśmiecania pamięci wywołuje <xref:System.Object.Finalize%2A> metodę obiektu w nieokreślonym czasie po obiekt jest określany jako nie jest już dostępny. Po <xref:System.Object.Finalize%2A> jest wywoływana, dodatkowy wyrzucania elementów bezużytecznych jest wymagany w celu zwolnienia obiektu. <xref:System.IDisposable.Dispose%2A> Metoda umożliwia obiektowi wywołującemu jawnie zwalniać zasoby na żądanie, starsze niż zasoby zostaną zwolnione, jeśli pole pozostanie na wyrzucanie elementów bezużytecznych. Po go czyści niezarządzane zasoby <xref:System.IDisposable.Dispose%2A> powinny wywoływać <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> metodę, aby umożliwić poinformować, że moduł odśmiecania pamięci <xref:System.Object.Finalize%2A> nie ma już wywołane; to eliminuje potrzebę stosowania dodatkowych wyrzucania elementów bezużytecznych i skraca okres istnienia obiektu.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, należy zaimplementować <xref:System.IDisposable>.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Jest bezpieczne pominąć ostrzeżenie od tej reguły, jeśli typ nie odwołuje się do niezarządzanego zasobu. W przeciwnym razie nie Pomijaj ostrzeżeń dla tej reguły, ponieważ nie można zaimplementować <xref:System.IDisposable> może spowodować, że zasoby niezarządzane stać się niedostępne lub rozłączania.

## <a name="example"></a>Przykład
 Poniższy przykład przedstawia typ, który implementuje <xref:System.IDisposable> wyczyścić niezarządzany zasób.

 [!code-csharp[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/CSharp/ca1049-types-that-own-native-resources-should-be-disposable_1.cs)]
 [!code-vb[FxCop.Design.UnmanagedResources#1](../code-quality/codesnippet/VisualBasic/ca1049-types-that-own-native-resources-should-be-disposable_1.vb)]

## <a name="related-rules"></a>Powiązane reguły
 [CA2115: Wywołaj funkcję GC.KeepAlive w przypadku korzystania z zasobów natywnych](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)

 [CA1816: Wywołaj poprawnie metodę GC.SuppressFinalize](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)

 [CA2216: Typy możliwe do likwidacji powinny deklarować finalizator](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

 [CA1001: Typy z polami możliwymi do likwidacji powinny być możliwe do likwidacji](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)

## <a name="see-also"></a>Zobacz także

- [Oczyszczanie zasobów niezarządzanych](/dotnet/standard/garbage-collection/unmanaged)
- [Wzorzec Dispose](/dotnet/standard/design-guidelines/dispose-pattern)