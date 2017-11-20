---
title: "Testy jednostkowe metod ogólnych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-test
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- generics, and unit tests
- unit tests, and generics
ms.assetid: ffc89814-a7df-44fc-aef5-dd3dfeb28a9b
caps.latest.revision: "47"
ms.author: douge
manager: douge
ms.openlocfilehash: 2a93a2af3f3d89a4970a949b42bea79b3641d53f
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="unit-tests-for-generic-methods"></a>Testy jednostkowe metod ogólnych
Możesz wygenerować testy jednostkowe metod ogólnych dokładnie tak jak w przypadku innych metod, zgodnie z opisem w [porady: tworzenie i uruchamianie testu jednostkowego](http://msdn.microsoft.com/en-us/5e0f43cf-5e51-48e2-9c98-0eb9324bdc48). Poniższe sekcje zawierają informacje i przykłady tworzenia testów jednostkowych dla metod generycznych.  
  
## <a name="type-arguments-and-type-constraints"></a>Argumenty typu i ograniczenia typu  
 Gdy [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] generuje testu jednostkowego dla klasy ogólnej, takich jak `MyList<T>`, generuje dwóch metod: Ogólne pomocnika i metody testowej. Jeśli `MyList<T>` ma co najmniej jednego ograniczenia typu, argumentu typu muszą spełniać wszystkie ograniczenia typu. Aby upewnić się, że ogólnego kodu w obszarze testu działa zgodnie z oczekiwaniami dla wszystkich dopuszczalna danych wejściowych, metody testowej wywołuje metodę pomocnika ogólnego z ograniczeniami, które mają zostać przetestowane.  
  
## <a name="examples"></a>Przykłady  
 Poniższe przykłady przedstawiają testów jednostkowych dla typów ogólnych:  
  
-   [Edytowanie testu kod wygenerowany przez](#EditingGeneratedTestCode). W tym przykładzie ma dwie sekcje wygenerowany kod testu i edytować kod testu. Widoczny jest sposób Edytuj kod testu raw, który jest generowany na podstawie metody rodzajowej metody przydatne testu.  
  
-   [Za pomocą ograniczenia typu](#TypeConstraintNotSatisfied). Ten przykład przedstawia testu jednostkowego dla metody ogólnej, który używa ograniczenia typu. Ograniczenie typu w tym przykładzie nie został spełniony.  
  
###  <a name="EditingGeneratedTestCode"></a>Przykład 1: Edytowanie kodu wygenerowanego testu  
 Kod testu w tej sekcji testów metodę kodu w obszarze testu o nazwie `SizeOfLinkedList()`. Ta metoda zwraca liczbę całkowitą, która określa liczbę węzłów w połączonej listy.  
  
 Pierwszy przykładowym kodzie w sekcji wygenerowanego kodu testu, zawiera kod testu nie do edycji wygenerowane przez Visual Studio Enterprise. Drugi przykład, w sekcji kodu testowego edytowany, pokazuje, jak można wprowadzić testowania funkcjonowania metodę SizeOfLinkedList dla dwóch różnych typów danych, `int` i `char`.  
  
 Ten kod ilustruje dwóch metod:  
  
-   metodę pomocnika testu `SizeOfLinkedListTestHelper<T>()`. Domyślnie metody pomocnika testu ma "TestHelper" w nazwie.  
  
-   Metoda testowa `SizeOfLinkedListTest()`. Każdej metody testowej jest oznaczona przez atrybut TestMethod.  
  
#### <a name="generated-test-code"></a>Kod wygenerowany Test  
 Poniższy kod testu został wygenerowany na podstawie `SizeOfLinkedList()` metody. Ponieważ jest to nie do edycji wygenerowany test, należy zmodyfikować do testowania poprawnie metody SizeOfLinkedList.  
  
```  
public void SizeOfLinkedListTestHelper<T>()  
{  
    T val = default(T); // TODO: Initialize to an appropriate value  
    MyLinkedList<T> target = new MyLinkedList<T>(val); // TODO: Initialize to an appropriate value  
    int expected = 0; // TODO: Initialize to an appropriate value  
    int actual;  
    actual = target.SizeOfLinkedList();  
    Assert.AreEqual(expected, actual);  
    Assert.Inconclusive("Verify the correctness of this test method.");  
}  
  
[TestMethod()]  
public void SizeOfLinkedListTest()  
{  
   SizeOfLinkedListTestHelper<GenericParameterHelper>();  
}  
```  
  
 W poprzednim kodzie parametr typu ogólnego jest `GenericParameterHelper`. Należy go podać określonych typów danych, można edytować, jak pokazano w poniższym przykładzie, można uruchomić testu bez konieczności edytowania tej instrukcji.  
  
#### <a name="edited-test-code"></a>Edytować kod testu  
 W poniższym kodzie metody testowej, a także metoda pomocnika test był edytowany aby je pomyślnie metody testowej kodu na mocy testu `SizeOfLinkedList()`.  
  
##### <a name="test-helper-method"></a>Testowanie metody pomocnika  
 Metoda pomocnika testu wykonuje następujące czynności, które odnoszą się do linii w kodzie etykietą kroki od 1 do 5.  
  
1.  Utwórz ogólne listy połączonej.  
  
2.  Dołącz czterech węzłów do listy połączonej. Typ danych zawartości te węzły jest nieznany.  
  
3.  Przypisz oczekiwanego rozmiaru połączonej listy do zmiennej `expected`.  
  
4.  Rzeczywisty rozmiar listy połączonej obliczeniowe i przypisz go do zmiennej `actual`.  
  
5.  Porównaj `actual` z `expected` w instrukcji potwierdzenia. Rzeczywiste nie jest równa oczekiwanej, test zakończy się niepowodzeniem.  
  
##### <a name="test-method"></a>Test — metoda  
 Metoda testowa jest kompilowany do kodu, który jest wywoływany, gdy uruchomienie testu o nazwie SizeOfLinkedListTest. Wykonuje następujące czynności, które odnoszą się do linii w kodzie etykietą krok 6 i 7.  
  
1.  Określ `<int>` podczas wywołania metody pomocnika, aby sprawdzić, czy test działa w przypadku `integer` zmiennych.  
  
2.  Określ `<char>` podczas wywołania metody pomocnika, aby sprawdzić, czy test działa w przypadku `char` zmiennych.  
  
```  
  
public void SizeOfLinkedListTestHelper<T>()  
{  
    T val = default(T);   
    MyLinkedList<T> target = new MyLinkedList<T>(val); // step 1  
    for (int i = 0; i < 4; i++) // step 2  
    {  
        MyLinkedList<T> newNode = new MyLinkedList<T>(val);  
        target.Append(newNode);  
    }  
    int expected = 5; // step 3  
    int actual;  
    actual = target.SizeOfLinkedList(); // step 4  
    Assert.AreEqual(expected, actual); // step 5  
}  
  
[TestMethod()]  
public void SizeOfLinkedListTest()   
{  
    SizeOfLinkedListTestHelper<int>();  // step 6  
    SizeOfLinkedListTestHelper<char>(); // step 7  
}  
```  
  
> [!NOTE]
>  Każdym uruchomieniu testu SizeOfLinkedListTest jego TestHelper metoda jest wywoływana dwa razy. Instrukcja assert musi zwrócić wartość true, zawsze dla testu do przekazania. Jeśli test ma wynik negatywny, może nie być wyczyść czy wywołanie określony `<int>` lub wywołania określonej `<char>` spowodował niepowodzenie. Aby znaleźć odpowiedzi, należy zbadać stos wywołań, lub można ustawić punktów przerwania w metodę testu, a następnie debugowania podczas wykonywania testu. Aby uzyskać więcej informacji, zobacz [porady: debugowanie podczas uruchamiania testu w rozwiązaniu ASP.NET](http://msdn.microsoft.com/Library/de4d7aa1-4a1e-467e-a19b-4a85ec245b8b).  
  
###  <a name="TypeConstraintNotSatisfied"></a>Przykład 2: Za pomocą ograniczenia typu  
 Ten przykład przedstawia testu jednostkowego dla metody ogólnej, który używa ograniczenia typu, który nie został spełniony. Pierwsza sekcja zawiera kod z projektu kodu w obszarze testu. Ograniczenie typu zostanie wyróżniona.  
  
 Druga sekcja zawiera kod z projektu testowego.  
  
#### <a name="code-under-test-project"></a>Projekt kodu w obszarze testu  
  
```  
using System;  
using System.Linq;  
using System.Collections.Generic;  
using System.Text;  
  
namespace ClassLibrary2  
{  
    public class Employee  
    {  
        public Employee(string s, int i)  
        {  
        }  
    }  
  
    public class GenericList<T> where T : Employee  
    {  
        private class Node  
        {  
            private T data;  
            public T Data  
            {  
                get { return data; }  
                set { data = value; }  
            }  
        }  
    }  
}  
```  
  
#### <a name="test-project"></a>Projekt testowy  
 Podobnie jak w przypadku wszystkich nowo wygenerowane testy jednostkowe, należy dodać do tego testu jednostkowego, aby był zwracany przydatne wyniki-niejednoznaczny Assert-instrukcje. Nie należy dodawać je do metody oznaczonej przez atrybut TestMethod, ale do metody "TestHelper", której dla tego testu o nazwie `DataTestHelper<T>()`.  
  
 W tym przykładzie parametr typu ogólnego `T` ma ograniczenie `where T : Employee`. To ograniczenie nie został spełniony w metodzie testowej. W związku z tym `DataTest()` metoda zawiera instrukcję Assert, która ostrzega o wymogu dostarczania ograniczenia typu, który został umieszczony na `T`. Komunikat niniejszych Assert o następującej treści:`("No appropriate type parameter is found to satisfies the type constraint(s) of T. " + "Please call DataTestHelper<T>() with appropriate type parameters.");`  
  
 Innymi słowy, gdy jest wywoływana `DataTestHelper<T>()` metody z metody testowej `DataTest()`, należy przekazać parametr typu `Employee` lub klasą pochodną `Employee`.  
  
 `using ClassLibrary2;`  
  
 `using Microsoft.VisualStudio.TestTools.UnitTesting;`  
  
 `namespace TestProject1`  
  
```  
{  
    [TestClass()]  
    public class GenericList_NodeTest  
    {  
  
        public void DataTestHelper<T>()  
            where T : Employee  
        {  
            GenericList_Shadow<T>.Node target = new GenericList_Shadow<T>.Node(); // TODO: Initialize to an appropriate value  
            T expected = default(T); // TODO: Initialize to an appropriate value  
            T actual;  
            target.Data = expected;  
            actual = target.Data;  
            Assert.AreEqual(expected, actual);  
            Assert.Inconclusive("Verify the correctness of this test method.");  
        }  
  
        [TestMethod()]  
        public void DataTest()  
        {  
            Assert.Inconclusive("No appropriate type parameter is found to satisfies the type constraint(s) of T. " +  
            "Please call DataTestHelper<T>() with appropriate type parameters.");  
        }  
    }  
}  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Anatomia testu jednostkowego](http://msdn.microsoft.com/en-us/a03d1ee7-9999-4e7c-85df-7d9073976144)   
 [Testowanie jednostek kodu](../test/unit-test-your-code.md)