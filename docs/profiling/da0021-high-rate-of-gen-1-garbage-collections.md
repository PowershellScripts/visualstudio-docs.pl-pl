---
title: "DA0021: Wysoki stopień odzyskiwania pamięci Gen 1 | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.performance.21
- vs.performance.DA0021
- vs.performance.rules.DA0021
ms.assetid: ebf5d9b3-a1ac-4688-8f0f-39a85f4dd15f
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8621dfbd3dea6f1c2dec7152aef586748f8e948a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="da0021-high-rate-of-gen-1-garbage-collections"></a>DA0021: Wysoki stopień odzyskiwania pamięci Gen 1
|||  
|-|-|  
|Identyfikator reguły|DA0021|  
|Kategoria|Sposób użycia programu .NET framework|  
|Metod profilowania|Wszystkie|  
|Komunikat|Istnieje stosunkowo wysokie tempo Gen 1 wyrzucania występuje. Jeśli zgodnie z projektem, większość struktur danych programu są przydzielane i utrwalane na dłuższy czas, to nie jest zazwyczaj problem. Jednak w przypadku niezamierzonego to zachowanie aplikacji może być przypinanie obiektów. Jeśli nie masz pewności, możesz zbierać .NET pamięci alokacji danych i obiektów okres istnienia informacje Aby poznać wzorzec przydzielania pamięci, który korzysta z aplikacji.|  
|Typ reguły|Informacje|  
  
 Gdy profilu można za pomocą próbkowania, pamięci platformy .NET lub metody kontencji zasobów, należy zebrać co najmniej 10 próbek do wyzwolenia tej reguły.  
  
## <a name="cause"></a>Przyczyna  
 Dane o wydajności systemu, które zostały zebrane podczas profilowania wskazują, że znaczna część obiekty struktury for.NET pamięci została odzyskana podczas generowania 1 wyrzucanie elementów bezużytecznych w porównaniu do zbierania danych 0 generacji.  
  
## <a name="rule-description"></a>Opis reguły  
 Program Microsoft .NET wspólnego języka środowiska wykonawczego (CLR) zapewnia mechanizm zarządzania automatyczne pamięci używane przez moduł Garbage Collector do odzyskać pamięci z obiektów, które nie jest już używane przez aplikację. Moduł zbierający elementy bezużyteczne to zorientowane na generowanie oparte na założeniu, że wiele są krótkim okresie. Zmienne lokalne, na przykład należy krótkim okresie. Nowo utworzone obiekty Uruchom podczas generowania 0 (gen 0), a następnie postępu na pokolenie 1 po ich przetrwać wyrzucanie elementów bezużytecznych Uruchom, a na koniec przejście do generacji 2 Jeśli aplikacja nadal używa ich.  
  
 Często i zazwyczaj bardzo wydajnie, są zebrane obiektów generacji 0. Obiekty w generacji 1 są zbierane rzadziej i mniej wydajne. Na koniec długotrwałe obiektów podczas generowania 2 powinny być gromadzone nawet rzadziej. Kolekcja generacji 2, czyli pełnego wyrzucania elementów bezużytecznych, uruchom również jest najbardziej kosztowna operacja.  
  
 Ta zasada uruchamiane w przypadku proporcjonalnie za dużo generacji 1 wyrzucania wystąpiły. Za dużo obiektów dość krótkim okresie przetrwać kolekcji pokolenia 0, ale będą w stanie mają być zbierane w kolekcji generacji 1, kosztów zarządzania pamięci może być nadmierne. Aby uzyskać więcej informacji, zobacz [kryzysami Średni czas życia](http://go.microsoft.com/fwlink/?LinkId=177835) post na informacje o wydajności Rico Mariani technologii w witrynie MSDN.  
  
## <a name="how-to-investigate-a-warning"></a>Jak badać ostrzeżenie  
 Kliknij dwukrotnie komunikat w oknie Lista błędów, aby przejść do [widoku znaczniki](../profiling/marks-view.md) danych profilowania. Znajdź **pamięci platformy .NET CLR\\# kolekcje pokolenia 0** i **pamięci platformy .NET CLR\\# pamięci Gen 1** kolumn. Określa, czy określone fazy wykonywania programu gdzie wyrzucanie elementów bezużytecznych występuje częściej. Porównanie tych wartości **% czasu potrzebnego na Odzyskiwanie** kolumny, aby zobaczyć, czy wzorzec przydziału pamięci zarządzanej powoduje nadmiernego pamięci nakład pracy osób.  
  
 Aby poznać wzorzec aplikacji użycia pamięci zarządzanej, profilu będzie ponownie działać alokacji pamięci a.NET pomiarów okres istnienia obiektu profilu i żądania.  
  
 Aby dowiedzieć się, jak poprawić wydajność kolekcji pamięci, zobacz [podstawy modułu zbierającego elementy bezużyteczne i wskazówki dotyczące wydajności](http://go.microsoft.com/fwlink/?LinkId=148226) w witrynie sieci Web firmy Microsoft. Uzyskać informacji o obciążenie automatyczne odzyskiwanie pamięci, zobacz [niepokrytego sterty obiektu dużych](http://go.microsoft.com/fwlink/?LinkId=177836).