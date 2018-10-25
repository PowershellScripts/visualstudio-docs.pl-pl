---
title: 'DA0010: Kosztowna funkcja GetHashCode | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAExpensiveGetHashCode
- vs.performance.DA0010
- vs.performance.rules.DA0010
- vs.performance.10
ms.assetid: 3987e21a-5b4f-45e4-8a33-6b3f0a472c08
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c4bb60104fa865cffa3e06ac088b92081e444457
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49877234"
---
# <a name="da0010-expensive-gethashcode"></a>DA0010: Expensive GetHashCode

|||  
|-|-|  
|Identyfikator reguły|DA0010|  
|Kategoria|Sposób użycia programu .NET framework|  
|Metod profilowania|Próbkowania<br /><br /> Pamięć .NET|  
|Komunikat|Funkcje GetHashCode powinny być tanie i nie alokować wszystkie pamięci. Mniejsza złożoność funkcji wartości skrótu, jeśli jest to możliwe.|  
|Typ komunikatu|Ostrzeżenie|  

## <a name="cause"></a>Przyczyna  
 Wywołania metody GetHashCode tego typu są znaczna część danych profilowania, lub metoda przydziela pamięć.  

## <a name="rule-description"></a>Opis reguły  
 Wyznaczania wartości skrótu jest techniką, szybko lokalizowania określonego elementu w dużych kolekcji. Ponieważ tabele skrótów mogą być duże i musi obsługiwać bardzo intensywny dostępu, tabele zbędnych danych powinna być wydajne. Domniemanie to wymaganie jest, że metody GetHashCode w programie .NET Framework nie należy przydzielić pamięci. Przydzielanie pamięci zwiększa obciążenie moduł odśmiecania pamięci i udostępnia metody do potencjalnych opóźnienia, jeśli okaże się niezbędne do uruchomienia wyrzucania elementów bezużytecznych w wyniku żądania alokacji.  

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Zmniejsz złożoność metody.