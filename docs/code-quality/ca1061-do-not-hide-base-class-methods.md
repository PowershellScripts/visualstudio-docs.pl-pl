---
title: "CA1061: Nie należy ukrywać metod klasy podstawowej | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1061
- DoNotHideBaseClassMethods
helpviewer_keywords:
- DoNotHideBaseClassMethods
- CA1061
ms.assetid: 0bda9dc8-87b4-4038-ab9d-563298387466
caps.latest.revision: "9"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 0c2cd6c6cfd06be965581d422b835014f09dd96b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1061-do-not-hide-base-class-methods"></a>CA1061: Nie należy ukrywać metod klasy podstawowej
|||  
|-|-|  
|TypeName|DoNotHideBaseClassMethods|  
|CheckId|CA1061|  
|Kategoria|Microsoft.Design|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Typ pochodny deklaruje metody o tej samej nazwie i z taką samą liczbę parametrów jako jeden z jego metod bazowych; co najmniej jeden z parametrów jest podstawowym typem odpowiadającym mu parametrem w metodzie podstawowej; a wszystkie pozostałe parametry mają typy, które są takie same jak wartości odpowiadających im parametrów w metodzie podstawowej.  
  
## <a name="rule-description"></a>Opis reguły  
 Metody w typie podstawowym jest ukryty przez metodę o identycznej nazwie w typie pochodnym, gdy parametr podpis Metoda pochodna różni się tylko typy, które są bardziej słabo pochodzące od odpowiednich typów w podpisie parametru metody podstawowej.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Aby naprawić naruszenie tej reguły, usuń lub zmień jego nazwę metody, zmienianie podpisu parametr tak, że metoda ukrywa metodę podstawową.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Nie pomijaj ostrzeżeń dla tej reguły.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono metodę, która narusza zasady.  
  
 [!code-csharp[FxCop.Design.HideBaseMethod#1](../code-quality/codesnippet/CSharp/ca1061-do-not-hide-base-class-methods_1.cs)]