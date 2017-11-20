---
title: "CA1710: Identyfikatory powinny mieć poprawny przyrostek | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA1710
- IdentifiersShouldHaveCorrectSuffix
helpviewer_keywords:
- IdentifiersShouldHaveCorrectSuffix
- CA1710
ms.assetid: 2b8e6dce-b4e8-4a66-ba9a-6b79be5bfe8c
caps.latest.revision: "20"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4fd4f23ab77e2b810d5064bd45e9f7d530e9844e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ca1710-identifiers-should-have-correct-suffix"></a>CA1710: Identyfikatory powinny mieć poprawny przyrostek
|||  
|-|-|  
|TypeName|IdentifiersShouldHaveCorrectSuffix|  
|CheckId|CA1710|  
|Kategoria|Microsoft.Naming|  
|Zmiana kluczowa|Kluczowa|  
  
## <a name="cause"></a>Przyczyna  
 Identyfikator nie ma odpowiedniego sufiksu.  
  
## <a name="rule-description"></a>Opis reguły  
 Konwencja nazwy typów, które rozszerzać niektórych typów podstawowych lub zawierają implementację niektórych interfejsów lub typy pochodzące z tych typów mieć sufiks, który jest skojarzony z typu podstawowego lub interfejs.  
  
 Konwencje nazewnictwa Podaj wygląd wspólnej dla bibliotek przeznaczonych środowisko uruchomieniowe języka wspólnego. Zmniejsza to nauki jest wymagany dla nowej biblioteki oprogramowania, którą można tworzyć bardziej niezawodne klienta, czy biblioteka został opracowany przez osobę, która ma doświadczenia w rozwijającym się kodu zarządzanego.  
  
 W poniższej tabeli wymieniono typy podstawowe i interfejsy, które administrator skojarzył sufiksy.  
  
|Interfejs podstawowy|Sufiks|  
|--------------------------|------------|  
|<xref:System.Attribute?displayProperty=fullName>|Atrybut|  
|<xref:System.EventArgs?displayProperty=fullName>|EventArgs|  
|<xref:System.Exception?displayProperty=fullName>|Wyjątek|  
|<xref:System.Collections.ICollection?displayProperty=fullName>|Kolekcja|  
|<xref:System.Collections.IDictionary?displayProperty=fullName>|Słownik|  
|<xref:System.Collections.IEnumerable?displayProperty=fullName>|Kolekcja|  
|<xref:System.Collections.Queue?displayProperty=fullName>|Kolekcji lub kolejki|  
|<xref:System.Collections.Stack?displayProperty=fullName>|Kolekcji lub stosu|  
|<xref:System.Collections.Generic.ICollection%601?displayProperty=fullName>|Kolekcja|  
|<xref:System.Collections.Generic.IDictionary%602?displayProperty=fullName>|Słownik|  
|<xref:System.Data.DataSet?displayProperty=fullName>|DataSet|  
|<xref:System.Data.DataTable?displayProperty=fullName>|Kolekcji lub elementu DataTable|  
|<xref:System.IO.Stream?displayProperty=fullName>|Strumień|  
|<xref:System.Security.IPermission?displayProperty=fullName>|Uprawnienie|  
|<xref:System.Security.Policy.IMembershipCondition?displayProperty=fullName>|Warunek|  
|Delegat obsługi zdarzeń.|EventHandler|  
  
 Typy, które implementują <xref:System.Collections.ICollection> i są uogólniony typ struktury danych, takimi jak słownika, stack lub queue, są dozwolone nazw, które zawierają istotne informacje o zamierzone użycie typu.  
  
 Typy, które implementują <xref:System.Collections.ICollection> i znajdują się, których nazwa kończy się wyrazem "Kolekcji" ma zbiór wybranych elementów. Na przykład kolekcja <xref:System.Collections.Queue> obiektów może mieć nazwy "QueueCollection". Z sufiksem "Collection" oznacza, że Członkowie kolekcji mogą być wyliczane przy użyciu `foreach` (`For Each` w [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) instrukcji.  
  
 Typy, które implementują <xref:System.Collections.IDictionary> mają nazwy, które kończą się słowem "Słownik" nawet wtedy, gdy typ implementuje również <xref:System.Collections.IEnumerable> lub <xref:System.Collections.ICollection>. Konwencje nazewnictwa sufiksem "Collection" i "Słownik" Użytkownicy rozróżnienia następujące wzorce dwóch wyliczenia.  
  
 Typy z sufiksem "Collection" wykonaj tego wzorca wyliczenia.  
  
```  
foreach(SomeType x in SomeCollection) { }  
```  
  
 Typy z sufiksem "Słownik" wykonaj tego wzorca wyliczenia.  
  
```  
foreach(SomeType x in SomeDictionary.Values) { }  
```  
  
 A <xref:System.Data.DataSet> obiekt składa się z kolekcją <xref:System.Data.DataTable> obiektów, które składają się z kolekcji <xref:System.Data.DataColumn?displayProperty=fullName> i <xref:System.Data.DataRow?displayProperty=fullName> obiektów, między innymi. Te kolekcje, wdrożenia <xref:System.Collections.ICollection> za pośrednictwem podstawowym <xref:System.Data.InternalDataCollectionBase?displayProperty=fullName> klasy.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Zmień nazwę typu, dzięki czemu jest on sufiks terminem poprawne.  
  
## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia  
 Jest bezpieczne pominąć ostrzeżenie do użycia z sufiksem "Collection", jeśli typ jest strukturą danych ogólnych, może zostać rozszerzony lub który będzie zawierać dowolny zestaw różnych elementów. W takim przypadku nazwę, która zawiera przydatne informacje dotyczące implementacji, wydajność lub z innymi charakterystykami struktury danych może być uzasadnione (na przykład BinaryTree). W przypadkach, gdy typ reprezentuje kolekcję określonego typu (na przykład StringCollection), nie Pomijaj ostrzeżenia od tej reguły, ponieważ sufiks wskazuje, że typ mogą być wyliczane przy użyciu `foreach` instrukcji.  
  
 Dla innych sufiksów nie Pomijaj ostrzeżenia od tej reguły. Sufiks umożliwia przeznaczenia być widoczne z nazwy typu.  
  
## <a name="related-rules"></a>Powiązanych reguł  
 [CA1711: Identyfikatory nie powinny mieć nieprawidłowych sufiksów](../code-quality/ca1711-identifiers-should-not-have-incorrect-suffix.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Atrybuty](/dotnet/standard/design-guidelines/attributes)   
 [Obsługa i wywoływanie zdarzeń](/dotnet/standard/events/index)  