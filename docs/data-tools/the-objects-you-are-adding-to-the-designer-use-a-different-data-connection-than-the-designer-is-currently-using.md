---
title: Obiekty dodawane do projektanta używają innego połączenia danych niż aktualnie używane przez projektanta
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: a2fb26fa8960c652feefa157fb04c31b9ed7abb9
ms.sourcegitcommit: f37affbc1b885dfe246d4b2c295a6538b383a0ca
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/02/2018
ms.locfileid: "37174198"
---
# <a name="the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer"></a>Obiekty, dodawane do projektanta używają innego połączenia danych niż projektanta

Obiekty, które są dodawane do projektanta Użyj innego połączenia danych niż aktualnie używane projektanta. Czy chcesz zastąpić połączenie używane przez projektanta?

Podczas dodawania elementów do **Object Relational Designer** (**O/R Designer**), wszystkie elementy, użyj jednego połączenia danych udostępnionych. (Na powierzchnię projektową reprezentuje <xref:System.Data.Linq.DataContext>, który używa pojedynczego połączenia dla wszystkich obiektów na powierzchni.) Ten komunikat pojawia się po dodaniu obiektu do projektanta, który korzysta z połączenia danych, która różni się od połączenia danych są obecnie używane przez projektanta. Aby rozwiązać ten problem, można zachować istniejące połączenie. W przypadku wprowadzenia ten wybór nie można dodać wybranego obiektu. Alternatywnie można dodać obiektu i zresetuj <xref:System.Data.Linq.DataContext> połączenia do nowego połączenia.

> [!NOTE]
> Jeśli klikniesz **tak**, klas wszystkie jednostki w **O/R Designer** są mapowane na nowe połączenie.

## <a name="to-replace-the-existing-connection-with-the-connection-used-by-the-selected-object"></a>Aby zastąpić istniejące połączenie połączenie używane przez wybrany obiekt

- Kliknij przycisk **Tak**.

    Zaznaczony obiekt zostanie dodany do **O/R Designer**i *DataContext.Connection* jest ustawiona na nowe połączenie.

## <a name="to-continue-to-use-the-existing-connection-and-cancel-adding-the-selected-object"></a>Aby nadal korzystać z istniejącego połączenia i anulowania Dodawanie wybranego obiektu

- Kliknij przycisk **nie**.

    Akcja została anulowana. *DataContext.Connection* pozostanie wartość istniejącego połączenia.

## <a name="see-also"></a>Zobacz także

- [Komunikaty narzędzia Object Relational Designer](../data-tools/o-r-designer-messages.md)
- [Narzędzi LINQ to SQL w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
