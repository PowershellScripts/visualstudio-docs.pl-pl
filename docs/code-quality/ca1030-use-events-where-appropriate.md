---
title: 'CA1030: Używaj zdarzeń wszędzie, gdzie jest to odpowiednie'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- UseEventsWhereAppropriate
- CA1030
helpviewer_keywords:
- CA1030
- UseEventsWhereAppropriate
ms.assetid: ea051367-deeb-40f9-9b65-eb818f1e133a
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 08f5ec37d38824ca640dd19827db3b1d355d0ad7
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49815642"
---
# <a name="ca1030-use-events-where-appropriate"></a>CA1030: Używaj zdarzeń wszędzie, gdzie jest to odpowiednie

|||
|-|-|
|TypeName|UseEventsWhereAppropriate|
|CheckId|CA1030|
|Kategoria|Microsoft.Design|
|Zmiana kluczowa|Bez podziału|

## <a name="cause"></a>Przyczyna
 Nazwy metody publiczne, protected lub private rozpoczyna się od jednego z następujących czynności:

- Dodatek

- RemoveOn

- Ogień

- Zgłoś

## <a name="rule-description"></a>Opis reguły
 Ta reguła wykrywa metody o nazwach, które normalnie mogą być używane dla zdarzeń. Zdarzenia wykonaj wzorzec projektowy obserwatora lub publikowania i subskrybowania; są one używane podczas zmiany stanu, w jeden obiekt musi zostać przekazany innych obiektów. Jeśli metoda jest wywoływana w odpowiedzi na jasno określoną zmianę stanu, metoda powinna być wywoływany przez program obsługi zdarzeń. Obiekty, które wywołują tę metodę, powinny wywoływać zdarzenia, a nie bezpośrednio metodę.

 Typowe przykłady zdarzeń znajdują się w aplikacji interfejsu użytkownika, gdy akcja użytkownika, takie jak kliknięcie przycisku powoduje, że segment kodu do wykonania. Model zdarzenia .NET Framework nie jest ograniczona do interfejsów użytkownika; powinno być używane wszędzie tam, gdzie muszą komunikować się, że stan zmieni się na co najmniej jeden obiekt.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Jeśli metoda jest wywoływana, gdy zmieni się stan obiektu, należy rozważyć zmianę projektu do korzystania z modelu zdarzenia .NET Framework.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Pomijaj ostrzeżeń dla tej reguły, jeśli metoda nie działa w programie .NET Framework model zdarzeń.