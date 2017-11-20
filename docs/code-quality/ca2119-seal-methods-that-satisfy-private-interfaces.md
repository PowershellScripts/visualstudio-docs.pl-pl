---
title: "CA2119: Zapieczętuj metody, które spełniają interfejsy prywatne | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- SealMethodsThatSatisfyPrivateInterfaces
- CA2119
helpviewer_keywords:
- CA2119
- SealMethodsThatSatisfyPrivateInterfaces
ms.assetid: 483d02e1-cfaf-4754-a98f-4116df0f3509
caps.latest.revision: "18"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f05b59ffc48b072d1a94ddfd405072d9663e6257
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca2119-seal-methods-that-satisfy-private-interfaces"></a>CA2119: Zapieczętuj metody, które spełniają interfejsy prywatne
|||  
|-|-|  
|TypeName|SealMethodsThatSatisfyPrivateInterfaces|  
|CheckId|CA2119|  
|Kategoria|Microsoft.Security|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Dziedziczone typu publicznego zawiera implementację przesłonięcia metody `internal` (`Friend` w języku Visual Basic) interfejsu.  
  
## <a name="rule-description"></a>Opis reguły  
 Metody interfejsu muszą powszechnej dostępności, które nie mogą zostać zmienione przez typ implementujący. Interfejs wewnętrzny tworzy kontraktu, który nie jest przeznaczony do implementacji spoza zestawu, który definiuje interfejs. Typu publicznego, który implementuje metody interfejsu wewnętrznego przy użyciu `virtual` (`Overridable` w języku Visual Basic) modyfikator zapewnia metody do zastąpienia przez typem pochodnym, która jest poza zestaw. Jeśli drugi typ w zestawu definiującego wywołuje metodę i oczekuje tylko wewnętrzny kontraktu, zachowanie jest zagrożona podczas zamiast przesłoniętej metody w zestawie poza jest wykonywana. Spowoduje to utworzenie luki w zabezpieczeniach.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Ustalenie naruszenie tej reguły, zapobiegania metody zastępowaniu poza zestaw przy użyciu jednej z następujących czynności:  
  
-   Zmień typ deklarujący `sealed` (`NotInheritable` w języku Visual Basic).  
  
-   Zmień dostępność elementu typ deklarujący do `internal` (`Friend` w języku Visual Basic).  
  
-   Usuń wszystkie konstruktory publiczne z typ deklarujący.  
  
-   Zaimplementuj metodę bez użycia `virtual` modyfikator.  
  
-   Implementuje jawnie metody.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Można bezpiecznie pominąć ostrzeżenie z tej reguły, jeśli po dokładne przeglądu, problemy z zabezpieczeniami nie istnieją, które może być możliwe, jeśli metoda zostanie przesłonięta poza zestaw.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie przedstawiono typu `BaseImplementation`, który narusza tę regułę.  
  
 [!code-cpp[FxCop.Security.SealMethods1#1](../code-quality/codesnippet/CPP/ca2119-seal-methods-that-satisfy-private-interfaces_1.cpp)]
 [!code-csharp[FxCop.Security.SealMethods1#1](../code-quality/codesnippet/CSharp/ca2119-seal-methods-that-satisfy-private-interfaces_1.cs)]
 [!code-vb[FxCop.Security.SealMethods1#1](../code-quality/codesnippet/VisualBasic/ca2119-seal-methods-that-satisfy-private-interfaces_1.vb)]  
  
## <a name="example"></a>Przykład  
 Poniższy przykład wykorzystuje implementacja metody wirtualnej poprzedniego przykładu.  
  
 [!code-cpp[FxCop.Security.SealMethods2#1](../code-quality/codesnippet/CPP/ca2119-seal-methods-that-satisfy-private-interfaces_2.cpp)]
 [!code-csharp[FxCop.Security.SealMethods2#1](../code-quality/codesnippet/CSharp/ca2119-seal-methods-that-satisfy-private-interfaces_2.cs)]
 [!code-vb[FxCop.Security.SealMethods2#1](../code-quality/codesnippet/VisualBasic/ca2119-seal-methods-that-satisfy-private-interfaces_2.vb)]  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejsy](/dotnet/csharp/programming-guide/interfaces/index)   
 [Interfejsy](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)