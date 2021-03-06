---
title: 'Porady: Tworzenie metod DataContext zamapowanych na procedury składowane i funkcje (Projektant O-R)'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e7ca32f1-50b3-48af-ad92-ceafd749296a
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: 8ae5fb4b3785bde0e092f68b62a9b030069a52aa
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942702"
---
# <a name="how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-or-designer"></a>Porady: Tworzenie metod DataContext zamapowanych na procedury składowane i funkcje (O/R Designer)

Można dodać procedur przechowywanych i funkcji do **O/R Designer** jako <xref:System.Data.Linq.DataContext> metody. Wywołanie metody i przekazując wymaganych parametrów uruchamia procedurę składowaną lub funkcję w bazie danych i zwraca dane w typie zwracanym <xref:System.Data.Linq.DataContext> metody. Aby uzyskać szczegółowe informacje na temat <xref:System.Data.Linq.DataContext> metod, zobacz [metody DataContext (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md).

> [!NOTE]
> Można również użyć procedur składowanych Aby zastąpić domyślne [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] zachowania w czasie wykonywania, który wykonuje wstawiania, aktualizacji i usuwa podczas zmiany są zapisywane z klas jednostek bazy danych. Aby uzyskać więcej informacji, zobacz [porady: przypisywanie procedur składowanych do wykonywania aktualizacji, wstawiania i usuwania (O/R Designer)](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md).

## <a name="create-datacontext-methods"></a>Tworzenie metod DataContext

Możesz utworzyć <xref:System.Data.Linq.DataContext> metody, przeciągając przechowywane procedury lub funkcji z <strong>Eksploratora serwera lub ** Eksplorator bazy danych</strong> na **O/R Designer**.

> [!NOTE]
> Zwracany typ wygenerowany <xref:System.Data.Linq.DataContext> metoda różni się w zależności od tego, gdzie porzucić procedury składowanej lub funkcji na **O/R Designer**. Upuszczenie elementów bezpośrednio na istniejącej klasy jednostki tworzy <xref:System.Data.Linq.DataContext> metody z typem zwracanym klasy jednostki. Upuszczenie elementów na pustym obszarem **O/R Designer** tworzy <xref:System.Data.Linq.DataContext> metodę, która zwraca typ wygenerowany automatycznie. Możesz zmienić typ zwracany <xref:System.Data.Linq.DataContext> metoda po dodaniu go do **metody** okienka. Aby sprawdzić lub zmienić typ zwracany <xref:System.Data.Linq.DataContext> metody, zaznacz ją i sprawdź **typie zwracanym** właściwość **właściwości** okna. Aby uzyskać więcej informacji, zobacz [porady: zmiana zwracanego typu metody DataContext (O/R Designer)](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md).

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-create-datacontext-methods-that-return-automatically-generated-types"></a>Aby utworzyć element DataContext metody, które zwracają automatycznie wygenerowane typy

1.  W **Eksploratora serwera** lub **Eksplorator bazy danych**, rozwiń węzeł **procedur składowanych** węzeł bazy danych, z którym pracujesz.

2.  Zlokalizuj odpowiednią procedurę składowaną i przeciągnij go na pustym obszarem **O/R Designer**.

     <xref:System.Data.Linq.DataContext> Metody jest tworzone z automatycznie wygenerowanego zwracany typ i pojawia się w **metody** okienka.

### <a name="to-create-datacontext-methods-that-have-the-return-type-of-an-entity-class"></a>Aby utworzyć metody DataContext, które mają zwracany typ klasę jednostki

1.  W **Eksploratora serwera** lub **Eksplorator bazy danych**, rozwiń węzeł **procedur składowanych** węzeł bazy danych, z którym pracujesz.

2.  Zlokalizuj odpowiednią procedurę składowaną i przeciągnij go do istniejącej klasy jednostki w **O/R Designer**.

     <xref:System.Data.Linq.DataContext> Metody jest tworzony z typem zwracanym klasy wybranej jednostki i pojawia się w **metody** okienka.

> [!NOTE]
> Informacje dotyczące zmiany istniejącego typu zwracanego <xref:System.Data.Linq.DataContext> metod, zobacz [porady: zmiana zwracanego typu metody DataContext (O/R Designer)](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md).

## <a name="see-also"></a>Zobacz także

- [Narzędzi LINQ to SQL w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [Metody DataContext (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md)
- [Wskazówki: Tworzenie LINQ do klas SQL](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [Wprowadzenie do LINQ w Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)
- [LINQ w C#](/dotnet/csharp/linq/linq-in-csharp)