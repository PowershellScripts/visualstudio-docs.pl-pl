---
title: 'CA1715: Identyfikatory powinny mieć poprawny prefiks'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1715
- IdentifiersShouldHaveCorrectPrefix
helpviewer_keywords:
- IdentifiersShouldHaveCorrectPrefix
- CA1715
ms.assetid: cf45f8df-6855-4cb6-a4e2-7cfed714cf2f
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: ad2e867b40bd8fc05215e7bb1d905a7d079eecf2
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49879853"
---
# <a name="ca1715-identifiers-should-have-correct-prefix"></a>CA1715: Identyfikatory powinny mieć poprawny prefiks

|||
|-|-|
|TypeName|IdentifiersShouldHaveCorrectPrefix|
|CheckId|CA1715|
|Kategoria|Microsoft.Naming|
|Zmiana kluczowa|Przerywanie — gdy wywoływane na interfejsach.<br /><br /> Bez podziału — gdy wywoływane w parametrach typu ogólnego.|

## <a name="cause"></a>Przyczyna
 Nazwa widocznego na zewnątrz interfejsu nie rozpoczyna się od wielkie litery "I".

 —lub—

 Nazwa parametru typu ogólnego na widocznych zewnętrznie typie lub metodzie nie rozpoczyna się od wielkiej litery t ".

## <a name="rule-description"></a>Opis reguły
 Według Konwencji nazwy niektórych elementów programowania zaczynać od określonego prefiksu.

 Nazwy interfejsów powinna rozpoczynać się wielką który "I" następuje innego wielką literą. Ta zasada zgłasza naruszenia nazwy interfejsu, takie jak "MyInterface" i "IsolatedInterface".

 Nazwy parametrów typu ogólnego powinien zaczynać się wielką t "i opcjonalnie może następować innego wielką literą. Ta zasada zgłasza naruszenia nazwy parametru typu ogólnego, takie jak "V" i "Type".

 Konwencje nazewnictwa Obejmij wygląd wspólnych bibliotek obiektu docelowego środowiska uruchomieniowego języka wspólnego. Zmniejsza to nauki, jest wymagany dla nowe biblioteki oprogramowania, która zwiększa poziom zaufania klientów, że biblioteka został opracowany przez osobę, która ma doświadczenie w tworzenie kodu zarządzanego.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Zmień nazwę identyfikatora, tak, aby poprawnie jest poprzedzana.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład
 **Poniższy kod przedstawia interfejs niepoprawnie nazwanych.**

 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_1.cpp)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_1.vb)]
 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_1.cs)]

## <a name="example"></a>Przykład
 **Poniższy przykład naprawia wcześniejszego naruszenia praw przez dodanie przedrostka interfejsu prefiksem "I".**

 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_2.cs)]
 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_2.cpp)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_2.vb)]

## <a name="example"></a>Przykład
 **Poniższy przykład pokazuje parametr niepoprawnie o nazwie typu ogólnego.**

 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_3.cpp)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_3.vb)]
 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_3.cs)]

## <a name="example"></a>Przykład
 **Poniższy przykład naprawia wcześniejszego naruszenia praw przez dodanie przedrostka parametr typu ogólnego przy użyciu t ".**

 [!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_4.cpp)]
 [!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_4.cs)]
 [!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_4.vb)]

## <a name="related-rules"></a>Powiązane reguły
 [CA1722: Identyfikatory nie powinny mieć niepoprawnego prefiksu](../code-quality/ca1722-identifiers-should-not-have-incorrect-prefix.md)