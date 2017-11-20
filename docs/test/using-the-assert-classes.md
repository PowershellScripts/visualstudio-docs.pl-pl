---
title: "Korzystanie z klas potwierdzeń | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-test
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Assert classes
- Assert statements
- unit tests, Assert statements
- unit tests, Assert classes
ms.assetid: da1b7a0d-4f1d-4d50-a07e-7b3ff60053f9
caps.latest.revision: "27"
ms.author: douge
manager: douge
ms.openlocfilehash: 443c3fe0ece064993655895606ad8603b96f6286
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="using-the-assert-classes"></a>Korzystanie z klas potwierdzeń
Aby sprawdzić określonych funkcji, należy użyć klas potwierdzeń UnitTestingFramework przestrzeni nazw. Kod metody w kodzie rozwoju wywiera metody testowej jednostki, ale tylko wtedy, gdy obejmują Assert-instrukcje zgłasza poprawność działania kodu.  
  
## <a name="kinds-of-asserts"></a>Typy z potwierdzeń  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting> Przestrzeń nazw zawiera kilka rodzajów klas potwierdzeń:  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert>  
  
 W metodę testu można wywołać metody klasy Assert, takich jak Assert.AreEqual() dowolną liczbę. Klasa Assert ma wiele metod do wyboru, a wiele z tych metod ma kilka przeciążeń.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.CollectionAssert>  
  
 Porównywanie kolekcji obiektów i sprawdź stan co najmniej jednej kolekcji, należy użyć klasy CollectionAssert.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert>  
  
 Klasa StringAssert służy do porównywania ciągów znaków. Ta klasa zawiera różne przydatne metody, takie jak StringAssert.Contains, StringAssert.Matches i StringAssert.StartsWith.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertFailedException>  
  
 Wyjątek AssertFailedException jest generowany, gdy test zakończy się niepowodzeniem. Test zakończy się niepowodzeniem, jeśli upłynie limit czasu, nieoczekiwany wyjątek lub zawiera instrukcję Assert, który zwraca wynik nie powiodło się.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertInconclusiveException>  
  
 AssertInconclusiveException jest generowany, gdy test powstaje niejednoznacznego. Zwykle Dodaj instrukcję Assert.Inconclusive do testu, które są nadal działa na wskazująca, że nie jest jeszcze gotowy do uruchomienia.  
  
> [!NOTE]
>  Strategia alternatywnych byłoby oznaczyć testu, który nie jest gotowy do uruchomienia z atrybutem Ignoruj. Ma to jednak wadą, który nie może łatwo wygenerować raport liczby testów się, że masz jeszcze na wdrożenie.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.UnitTestAssertException>  
  
 Jeśli piszesz nowej klasy wyjątku Assert, o tej klasy, które dziedziczą z klasy podstawowej UnitTestAssertException ułatwia identyfikację wyjątku, ponieważ błąd potwierdzenia zamiast nieoczekiwany wyjątek w kodzie testowym lub produkcyjnym.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.ExpectedExceptionAttribute>  
  
 Dekoracji metody testowej z atrybutem ExpectedExceptionAttribute, jeśli chcesz, aby metody testowej, aby sprawdzić, czy wyjątek może zostać wygenerowany przez metody w kodzie Programowanie w rzeczywistości został zgłoszony w tej metodzie.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting>   
 [Tworzenie i Uruchamianie testów jednostkowych dla istniejącego kodu](http://msdn.microsoft.com/en-us/e8370b93-085b-41c9-8dec-655bd886f173)