---
title: Projektant przepływu pracy — umożliwia przeglądanie i wybieranie typu .NET, okno dialogowe
ms.date: 11/04/2016
ms.topic: conceptual
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- TypeBrowser.UI
- ActivityTypeResolver.UI
ms.assetid: 864b60b6-a070-4e5c-aa5b-a25341b57ea6
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 686969c233f50dd1df743590206966183be48da9
ms.sourcegitcommit: 206e738fc45ff8ec4ddac2dd484e5be37192cfbd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/03/2018
ms.locfileid: "39513201"
---
# <a name="browse-and-select-a-net-type-dialog-box"></a>Wyszukiwanie i wybieranie typu .NET, okno dialogowe

W **właściwości** okien, okien dialogowych lub projektantów, takich jak projektanta zmiennych, po wybraniu **vyhledat typy** z listy typów danych, jest **Wyszukaj i wybierz typ architektury .NET** okno dialogowe (określone w formie skróconej jako "Przeglądarka typu"). W tym oknie można wybrać typ z widoku drzewa, zespołów i projektów.

To okno dialogowe są stosowane w wielu scenariuszy użytkownika, w tym następujące czynności:

-   Podczas ustawiania typ zmiennej lub argumentu.

-   Podczas wybierania typu ogólnego działania.

-   Podczas dodawania instrukcji catch w <xref:System.Activities.Statements.TryCatch> działania.

> [!NOTE]
> Przeglądarki typu można wyświetlić typy tablicowe nierówne w języku Visual Basic, ale typy nie wielowymiarowej tablicy. Zobacz [nierówne tablic](http://go.microsoft.com/fwlink/?LinkId=195226) i [tablic wielowymiarowych](http://go.microsoft.com/fwlink/?LinkId=195227) Aby uzyskać szczegółowe informacje.

## <a name="selecting-a-value-or-reference-type-from-the-type-browser"></a>Wybranie wartości lub typem referencyjnym, za pomocą przeglądarki typu

### <a name="to-select-a-value-or-reference-type-from-the-type-browser"></a>Aby wybrać typ wartości lub odwołania za pomocą przeglądarki typu

1.  W **nazwy typu** wprowadź nazwę typu, którego chcesz używać.

2.  Wykonaj jedną z następujących czynności:

    -   Gdy nazwa typu, którego chcesz używać pojawi się w drzewie w **nazwy typu** pole, kliknij dwukrotnie typu, aby go zaznaczyć.

    -   Wpisz małej liczby znaków w **nazwy typu** pole, aby jednoznacznie identyfikują typ, który chcesz użyć, a następnie naciśnij klawisz enter, aby wybrać typ

### <a name="to-select-a-generic-type-from-the-type-browser"></a>Aby wybrać typ ogólny z przeglądarki typu

1.  W **nazwy typu** , wpisz nazwę typu, którego chcesz używać.

2.  Gdy nazwa typu, którego chcesz używać pojawi się w drzewie w **nazwy typu** pole, kliknij typ, wybierz ją, aby spowodować, że pola listy rozwijanej są wyświetlane.

     Wybierz typ, który chcesz użyć do Zamknij ogólnego z list rozwijanych, a następnie kliknij przycisk **OK**.

## <a name="types-displayed-in-the-type-browser"></a>Typy wyświetlonej w przeglądarce typu

Typy wyświetlonej w przeglądarce typu mogą się różnić w zależności od tego, jak przeglądarki typu została uruchomiona. Jeśli przeglądarka typów został uruchomiony z projektu przepływu pracy wewnątrz **vs2010**, domyślnie wszystkich typów w przywoływanych zestawach i przywoływane projekty nie są wyświetlane. Jeśli przeglądarka typów został uruchomiony z poza **vs2010** projektu systemowe (takie jak aplikacja rehostowanym przepływu pracy lub autonomiczny plik przepływu pracy), a następnie domyślnie są wyświetlane typy z wszystkie zestawy, ładowane w domenie aplikacji .

Typy w przeglądarce typu mogą być filtrowane przez deweloperów projektanta działań. Dla danego działania może zostać wyświetlony tylko podzbiór typów. Na przykład w <xref:System.Activities.Statements.TryCatch> działania tylko typy pochodne <xref:System.Exception> są wyświetlane w przeglądarce typu.

## <a name="filtering-search-results-in-the-type-browser"></a>Filtrowanie wyników wyszukiwania w przeglądarce typu

Lista typów w **nazwy typu** pole pobiera krótszy, ponieważ wpisz więcej znaków w celu znalezienia dopasowania. Tylko typy, których nazwa fullyqualified zaczyna się od ciągu, które zostały wpisane lub typów, w której krótka nazwa zaczyna się od ciągu, które zostały wpisane zostaną wyświetlone na liście filtrowane.

Na przykład:

1.  Wpisywanie **operacji** odpowiada <xref:System.OperationCanceledException> , ale nie <xref:System.InvalidOperationException>. Aby dopasować <xref:System.InvalidOperationException>, zacznij pisać System.I lub jest nieprawidłowy.

2.  Wpisywanie **ogólny** odpowiada <xref:System.GenericUriParser> , ale nie typy w <xref:System.Collections.Generic> przestrzeni nazw. Aby wyszukać typów w <xref:System.Collections.Generic> przestrzeni nazw, wpisz w pełni kwalifikowaną nazwę przestrzeni nazw.

## <a name="selecting-a-service-contract-using-the-type-browser-dialog"></a>Wybieranie kontraktu usługi, korzystając z okna dialogowego przeglądarki typu

Wybierając typ kontraktu usługi, przeglądarki typu zawiera tylko typy, które mają <xref:System.ServiceModel.ServiceContractAttribute> atrybutu.

## <a name="see-also"></a>Zobacz także

- [Używanie projektantów działań](../workflow-designer/using-the-activity-designers.md)