---
title: 'CA1026: Domyślne parametry nie powinny być używane'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1026
- DefaultParametersShouldNotBeUsed
helpviewer_keywords:
- CA1026
- DefaultParametersShouldNotBeUsed
ms.assetid: 09643415-36ef-4d0f-9411-5721e14e2512
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ec4a248be45489eafcbd208329a52cfc06d8237f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49825354"
---
# <a name="ca1026-default-parameters-should-not-be-used"></a>CA1026: Domyślne parametry nie powinny być używane

|||
|-|-|
|TypeName|DefaultParametersShouldNotBeUsed|
|CheckId|CA1026|
|Kategoria|Microsoft.Design|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Typ widoczny na zewnątrz zawiera widoczne na zewnątrz metodę, która korzysta z domyślnego parametru.

## <a name="rule-description"></a>Opis reguły
 Metody, z wykorzystaniem parametrów domyślnych są dozwolone w ramach Common Language Specification (CLS); jednak CLS umożliwia kompilatory ignorują wartości, które są przypisane do tych parametrów. Kod, który jest przeznaczony dla kompilatory, które będzie ignorować domyślne wartości parametrów należy jawnie określić argumenty dla każdego parametru domyślnego. Aby zapewnić odpowiednie zachowanie w językach programowania, metody, z wykorzystaniem parametrów domyślnych należy zastąpić przeciążeniami metod, które dostarczają parametry domyślne.

 Kompilator ignoruje wartości domyślne parametrów dla rozszerzenia zarządzane, dla języka C++, gdy uzyskuje dostęp do kodu zarządzanego. Kompilator języka Visual Basic obsługuje metody, które mają domyślne parametry, które używają [opcjonalnie](/dotnet/visual-basic/language-reference/modifiers/optional) — słowo kluczowe.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, należy zastąpić metodę, która korzysta z domyślnych parametrów, które dostarczają parametry domyślne przeciążeniami metod.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład
 Poniższy kod przedstawia metodę, która korzysta z domyślnych parametrów i przeciążone metody, które zapewniają podobne funkcje.

 [!code-vb[FxCop.Design.DefaultParameters#1](../code-quality/codesnippet/VisualBasic/ca1026-default-parameters-should-not-be-used_1.vb)]

## <a name="related-rules"></a>Powiązane reguły
 [CA1025: Zastąp powtarzające się argumenty tablicą parametrów](../code-quality/ca1025-replace-repetitive-arguments-with-params-array.md)

## <a name="see-also"></a>Zobacz także
 [Niezależność od języka i składniki niezależne od języka](/dotnet/standard/language-independence-and-language-independent-components)