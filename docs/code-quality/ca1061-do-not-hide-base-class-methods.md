---
title: 'CA1061: Nie należy ukrywać metod klasy bazowej'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1061
- DoNotHideBaseClassMethods
helpviewer_keywords:
- DoNotHideBaseClassMethods
- CA1061
ms.assetid: 0bda9dc8-87b4-4038-ab9d-563298387466
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: da132ba941c448f6323199d8baca86841d192ecf
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49924125"
---
# <a name="ca1061-do-not-hide-base-class-methods"></a>CA1061: Nie należy ukrywać metod klasy bazowej

|||
|-|-|
|TypeName|DoNotHideBaseClassMethods|
|CheckId|CA1061|
|Kategoria|Microsoft.Design|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Typ pochodny deklaruje metodę o takiej samej nazwie i z taką samą liczbę parametrów jako jeden z jego metod bazowych; co najmniej jeden z parametrów jest podstawowym typem odpowiadającym mu parametrem w metodzie podstawowej; i wszelkie pozostałe parametry mają typy, które są identyczne z odpowiednich parametrów w metody podstawowej.

## <a name="rule-description"></a>Opis reguły
 Metoda w typie podstawowym jest ukryta przez metodę o identycznej nazwie w typie pochodnym, gdy Sygnatura parametru metody pochodnej różni się tylko typami, które są słabiej dziedziczone niż odpowiadające typy w sygnaturze parametru metody podstawowej.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Aby naprawić naruszenie tej zasady, usuń lub zmień nazwę metody lub zmienić podpis parametru metody nie ukrywa metody podstawowej.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Nie pomijaj ostrzeżeń dla tej reguły.

## <a name="example"></a>Przykład
 Poniższy przykład przedstawia metodę, która narusza regułę.

 [!code-csharp[FxCop.Design.HideBaseMethod#1](../code-quality/codesnippet/CSharp/ca1061-do-not-hide-base-class-methods_1.cs)]