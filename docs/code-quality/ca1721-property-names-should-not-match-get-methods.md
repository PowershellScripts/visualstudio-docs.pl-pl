---
title: 'CA1721: Nazwy właściwości nie powinny odpowiadać metodom Get'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
helpviewer_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
ms.assetid: 45a0e853-1f06-4688-af1b-cc634409e295
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 26f6e23a340ec018f766477f0bdce089a43ca3e4
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/13/2018
ms.locfileid: "45549680"
---
# <a name="ca1721-property-names-should-not-match-get-methods"></a>CA1721: Nazwy właściwości nie powinny odpowiadać metodom Get

|||
|-|-|
|TypeName|PropertyNamesShouldNotMatchGetMethods|
|CheckId|CA1721|
|Kategoria|Microsoft.Naming|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Nazwa publicznego lub chronionego elementu członkowskiego zaczyna się od "Get" i odpowiada nazwie właściwości publicznej lub chronionej. Na przykład typ, który zawiera metodę o nazwie "Getcolor —" i właściwość, która nosi nazwę "Color" narusza tę regułę.

## <a name="rule-description"></a>Opis reguły
 Metody GET i właściwości powinny mieć nazwy, które wyraźnie odróżniają ich funkcje.

 Konwencje nazewnictwa Obejmij wygląd wspólnych bibliotek obiektu docelowego środowiska uruchomieniowego języka wspólnego. Ten spójności skraca czas, są wymagane, aby dowiedzieć się nowa Biblioteka oprogramowania, która zwiększa poziom zaufania klientów, że biblioteka został opracowany przez osobę, która ma doświadczenie w tworzenie kodu zarządzanego.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Zmień nazwę, tak aby nazwę metody, która jest poprzedzony znakiem "Get" nie pasuje.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

> [!NOTE]
> To ostrzeżenie, mogą zostać wyłączone, jeśli metoda Get jest spowodowany przez zaimplementowanie interfejsu iextenderprovider —.

## <a name="example"></a>Przykład
 Poniższy przykład zawiera metody i właściwości, które spełniają tej reguły.

 [!code-csharp[FxCop.Naming.GetMethod#1](../code-quality/codesnippet/CSharp/ca1721-property-names-should-not-match-get-methods_1.cs)]
 [!code-vb[FxCop.Naming.GetMethod#1](../code-quality/codesnippet/VisualBasic/ca1721-property-names-should-not-match-get-methods_1.vb)]

## <a name="related-rules"></a>Powiązane reguły
 [CA1024: Używaj właściwości wszędzie tam, gdzie jest to odpowiednie](../code-quality/ca1024-use-properties-where-appropriate.md)