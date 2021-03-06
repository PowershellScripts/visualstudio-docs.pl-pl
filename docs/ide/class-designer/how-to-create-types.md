---
title: 'Porady: tworzenie typów za pomocą Projektanta klas'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- VS.Clr.ClrAttributesDialog
helpviewer_keywords:
- custom attributes, applying
- class diagrams, creating types
- classes [Visual Studio], creating with Class Designer
- Class Designer [Visual Studio], creating classes
- types [Visual Studio], class diagrams
- attributes [Visual Studio], applying custom
ms.assetid: 94458c31-28bc-40e2-9737-85868788a0e5
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 769bcfa202961c5a492e4fcb5af8e522b9052059
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49842264"
---
# <a name="how-to-create-types-by-using-class-designer"></a>Porady: Tworzenie typów za pomocą projektanta klas

Do projektowania nowych typów dla C# i projektach języka Visual Basic, należy je utworzyć na diagramie klasy. Aby wyświetlić istniejące typy, zobacz [porady: wyświetlanie istniejących typów](how-to-view-existing-types.md).

##  <a name="CreateType"></a> Utwórz nowy typ

1.  W **przybornika**w obszarze **projektanta klas**, przeciągnij jeden z nich do diagramu klasy:

    -   **Klasa** lub **klasy abstrakcyjnej**

    -   **Enum**

    -   **Interface**

    -   **Struktura** (VB) lub **struktury** (C#)

    -   **Delegate**

    -   **Moduł** (tylko w języku VB)

2.  Nadaj nazwę typowi. Następnie wybierz jego poziom dostępu.

3.  Wybierz plik, do którego chcesz dodać kod początkowy dla typu:

    -   Aby utworzyć nowy plik i dodać go do bieżącego projektu, wybierz **Utwórz nowy plik** i nazwę pliku.

    -   Aby dodać kod do istniejącego pliku, wybierz **Dodaj do istniejącego pliku**.

         Jeśli rozwiązanie ma projektu, który udostępnia kod przez wiele aplikacji, możesz dodać nowy typ do diagramu klas w projekcie aplikacji, ale tylko jeśli odpowiadający plik klasy znajduje się w tym samym projekcie aplikacji lub znajduje się w udostępnionym projekcie.

4.  Teraz dodaj inne elementy, aby zdefiniować typ:

    |||
    |-|-|
    |**Aby uzyskać**|**Add**|
    |Klasy, klasy abstrakcyjne, struktury i obiekty struct|Metody, właściwości, pola, zdarzenia, konstruktory (metoda), destruktory (metoda) i stałe, które określają typ|
    |Wyliczenia|Wartości pól, które tworzą wyliczenie|
    |Interfejsy|Metody, właściwości i zdarzenia, które tworzą interfejs|
    |Delegate|Parametry, które definiują obiekt delegowany|
    |Moduł|Metody, właściwości, pola, zdarzenia, konstruktory (metoda) i stałe, które określają moduł|

     Zobacz [tworzenie elementów członkowskich](creating-and-configuring-type-members.md#create-members).

##  <a name="CustAttributeType"></a> Zastosuj atrybut niestandardowy do typu

1. Kliknij typ kształtu na diagramie klasy.

2. W **właściwości**obok pozycji **atrybuty niestandardowe** właściwości dla typu, kliknij przycisk wielokropka (...).

3. Dodaj jeden lub więcej atrybutów niestandardowych, jeden na wiersz. Nie otaczaj ich nawiasami kwadratowymi.

   Atrybuty niestandardowe są stosowane do typu.

##  <a name="CustAttributeMember"></a> Zastosuj atrybut niestandardowy do elementu członkowskiego typu

1. Kliknij nazwę składowej w jej kształcie typu na diagramie klasy lub kliknij jej wiersz w oknie Szczegóły klasy.

2. W **właściwości**, Znajdź elementu członkowskiego **atrybuty niestandardowe** właściwości.

3. Dodaj jeden lub więcej atrybutów niestandardowych, jeden na wiersz. Nie otaczaj ich nawiasami kwadratowymi.

   Atrybuty niestandardowe są stosowane do typu.

## <a name="see-also"></a>Zobacz także

- [Porady: Tworzenie dziedziczenia między typami](how-to-create-inheritance-between-types.md)
- [Porady: Tworzenie skojarzeń między typami](how-to-create-associations-between-types.md)
- [Tworzenie i konfigurowanie składowych typu](creating-and-configuring-type-members.md)
- [Praca z diagramami klas](working-with-class-diagrams.md)
- [Projektowanie klas i typów](designing-and-viewing-classes-and-types.md)
