---
title: 'Da0013: znaczące Wykorzystanie String.Split lub String.Substring | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.13
- vs.performance.rules.DAAvoidStringSubstr
- vs.performance.DA0013
- vs.performance.rules.DA0013
helpviewer_keywords:
- vs.performance.13
- vs.performance.rules.DA0013
ms.assetid: f501f423-bef9-4e08-bf96-c9ac9957e5a2
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 722277e65a30d8c40cc245123120650108ebc560
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49831461"
---
# <a name="da0013-high-usage-of-stringsplit-or-stringsubstring"></a>DA0013: Znaczące wykorzystanie String.Split lub String.Substring

|||  
|-|-|  
|Identyfikator reguły|DA0013 ZNACZĄCE|  
|Kategoria|Wskazówki dotyczące użycia programu .NET framework|  
|Metod profilowania|Próbkowania|  
|Komunikat|Należy rozważyć ograniczenie użycia funkcji String.Split i String.Substring.|  
|Typ reguły|Ostrzeżenie|  

## <a name="cause"></a>Przyczyna  
 Wywołania metod System.String.Split lub System.String.Substring jest znaczna część danych profilowania. Należy rozważyć użycie System.String.IndexOf lub System.String.IndexOfAny, jeśli testujesz istnienie podciągów w ciągu.  

## <a name="rule-description"></a>Opis reguły  
 Metoda Podziel operuje na obiekt ciągu i zwraca nową tablicę ciągów, która przechowuje podciągów z oryginalnego. Funkcja przydziela pamięć dla obiektu zwróconej tablicy i przydziela nowy obiekt ciągu dla każdego elementu tablicy, które znajdzie. Podobnie SUBSTR — metoda operuje na obiekt ciągu i zwraca nowy ciąg, który jest odpowiednikiem żądanego podciąg.  

 Jeśli zarządzanie alokacji pamięci ma kluczowe znaczenie dla aplikacji, należy rozważyć użycie alternatywy dla funkcji String.Split i String.Substr metod. Na przykład służy metoda IndexOf lub IndexOfAny aby zlokalizować podciąg określonego w ciągu znaków ciągu bez tworzenia nowego wystąpienia klasy String.  

## <a name="how-to-investigate-a-warning"></a>Jak badać ostrzeżenie  
 Kliknij dwukrotnie komunikat w **lista błędów** okna, aby przejść do [widok szczegółów funkcji](../profiling/function-details-view.md) pobierania próbek danych jej profilu. Sprawdź wywołania funkcji można znaleźć w sekcjach program najczęściej wykorzystać System.String.Split lub System.String.Substr metod. Jeśli to możliwe należy użyć metody IndexOf lub IndexOfAny aby zlokalizować podciąg określonego w ciągu znaków ciągu bez tworzenia nowego wystąpienia klasy String.