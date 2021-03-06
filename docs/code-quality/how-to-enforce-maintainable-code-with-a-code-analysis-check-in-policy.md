---
title: 'Porady: wymuszanie kodu za pomocą zasad ewidencjonowania analizy kodu'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- code analysis, check-in policies
ms.assetid: d1b3b04f-4dd9-40e6-b2d4-b414d33fb647
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f0121efb2e226b2407eee7eea50354a80482b1cc
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49892094"
---
# <a name="how-to-enforce-maintainable-code-with-a-code-analysis-check-in-policy"></a>Porady: Wymuszanie kodu łatwego w utrzymaniu za pomocą zasad analizy kodu zaewidencjonowania

Deweloperzy mogą używać narzędzia metryki kodu do mierzenie złożoności i łatwości konserwacji kodu, ale nie można wywołać metryki kodu jako części zasad ewidencjonowania. Jednak można włączyć reguły analizy kodu, które sprawdza zgodność kodu z normami metryki kodu i Wymuszanie reguł za pomocą zasad ewidencjonowania. Aby uzyskać więcej informacji na temat metryki kodu, zobacz [kodu wartości metryk](../code-quality/code-metrics-values.md).

Można włączyć głębokość dziedziczenia, sprzężenia klas, indeks łatwości utrzymania i złożoności wymuszanie kodu łatwego w utrzymaniu za pomocą zasad ewidencjonowania analizy kodu. Wszystkie cztery te zasady znajdują się w kategorii "Reguły utrzymania kodu" w edytorze zasad analizy kodu.

Administratorzy kontroli wersji serwera Team Foundation można dodać reguły utrzymania kodu analizy kodu do wymagań zasad ewidencjonowania. Te ewidencjonowania zasadami wymagających deweloperów uruchomić analizę kodu na podstawie tych reguł zmian przed zainicjowaniem ewidencjonowania.

## <a name="to-open-the-code-analysis-policy-editor"></a>Aby otworzyć Edytor zasad analizy kodu

1. W **Team Explorer**, kliknij prawym przyciskiem myszy projekt, kliknij przycisk **ustawienia projektu**, a następnie kliknij przycisk **kontroli źródła**.

     **Kontroli źródła** pojawi się okno dialogowe.

2. Na **zasad ewidencjonowania** kartę, a następnie kliknij przycisk **Dodaj**.

     **Dodaj zasady ewidencjonowania** pojawi się okno dialogowe.

3. W **zasad ewidencjonowania** listy wybierz **analizy kodu** pole wyboru, a następnie kliknij przycisk **OK**.

     **Edytor zasad analizy kodu** pojawi się okno dialogowe.

## <a name="to-enable-code-analysis-maintainability-rules"></a>Aby włączyć reguły utrzymania kodu analizy kodu

1. W **Edytor zasad analizy kodu** dialogowego **ustawienia reguły**, rozwiń węzeł **reguły utrzymania kodu** węzła.

2. Zaznacz pola wyboru dla następujących reguł:

   - Głębokość dziedziczenia: **CA1501 AvoidExcessiveInheritance** — próg: ostrzeżenie w więcej niż 5 poziomów w głąb

   - Złożoność: **CA1502 AvoidExcessiveComplexity** — próg: ostrzeżenie na więcej niż 25

   - Indeks łatwości utrzymania: **CA1505 AvoidUnmaintainableCode** — próg: ostrzeżenie na mniej niż 20

   - Sprzężenia klas: **CA1506 AvoidExcessiveClassCoupling** — próg: ostrzeżenie w więcej niż 80 dla klasy i więcej niż 30 dla metody

     Ponadto naruszenie reguły, aby zapobiec pomyślnej kompilacji, wybierz **Traktuj ostrzeżenie jako błąd** pole wyboru obok opis reguły.

3. Kliknij przycisk **OK**. Nowe zasady ewidencjonowania dotyczy teraz przyszłych zaewidencjonowania.

## <a name="see-also"></a>Zobacz także

- [Wartości metryk kodów](../code-quality/code-metrics-values.md)
- [Tworzenie i używanie zasad ewidencjonowania analizy kodu](../code-quality/creating-and-using-code-analysis-check-in-policies.md)