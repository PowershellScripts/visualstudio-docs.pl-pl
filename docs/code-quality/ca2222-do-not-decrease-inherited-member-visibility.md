---
title: 'CA2222: Nie zmniejszaj widoczności dziedziczonego elementu członkowskiego'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotDecreaseInheritedMemberVisibility
- CA2222
helpviewer_keywords:
- DoNotDecreaseInheritedMemberVisibility
- CA2222
ms.assetid: 066c8675-381f-43cc-956c-d757cc494028
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 9dcf92e2a5cdfb7f83a84c55b222aabf415fcfe0
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2018
ms.locfileid: "45545664"
---
# <a name="ca2222-do-not-decrease-inherited-member-visibility"></a>CA2222: Nie zmniejszaj widoczności dziedziczonego elementu członkowskiego

|||
|-|-|
|TypeName|DoNotDecreaseInheritedMemberVisibility|
|CheckId|CA2222|
|Kategoria|Microsoft.Usage|
|Zmiana kluczowa|Bez podziału|

## <a name="cause"></a>Przyczyna

Prywatną metodę w niezamknięty typ ma podpis, który jest identyczny z publiczną metodę zadeklarowane w typie podstawowym. Metoda prywatna nie jest ostateczny.

## <a name="rule-description"></a>Opis reguły

Nie należy zmieniać modyfikatora dostępu dla dziedziczonych elementów członkowskich. Zmiana dziedziczonej składowej na prywatną nie uniemożliwia wywołującym uzyskania dostępu do implementacji metody klasy podstawowej. Jeśli element członkowski składa się prywatny i typ jest niezapieczętowany, typy dziedziczące wywołać ostatniego publicznych implementacji metody w hierarchii dziedziczenia. Jeśli musisz zmienić modyfikator dostępu, metoda powinna być oznaczona jako ostatecznego lub jego typ powinny być zapieczętowane tak, aby zapobiec zastąpieniu metody.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia

Aby naprawić naruszenie tej zasady, należy zmienić dostęp jako nieprywatny. Alternatywnie Jeśli język programowania obsługuje tę funkcję, można wprowadzić metody końcowego.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia

Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład

Poniższy przykład pokazuje typ, który narusza tę regułę.

[!code-vb[FxCop.Usage.InheritedPublic#1](../code-quality/codesnippet/VisualBasic/ca2222-do-not-decrease-inherited-member-visibility_1.vb)]
[!code-csharp[FxCop.Usage.InheritedPublic#1](../code-quality/codesnippet/CSharp/ca2222-do-not-decrease-inherited-member-visibility_1.cs)]