---
title: 'Wskazówki: Tworzenie klasy LINQ do SQL za pomocą pojedynczej tabeli dziedziczenia (Projektant O-R)'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
ms.assetid: 63bc6328-e0df-4655-9ce3-5ff74dbf69a4
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: 943b75c9c5f9c0c32ab02b5e73c07282728e0beb
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49864734"
---
# <a name="walkthrough-create-linq-to-sql-classes-by-using-single-table-inheritance-or-designer"></a>Przewodnik: Tworzenie LINQ do klas SQL za pomocą pojedynczej tabeli dziedziczenia (O/R Designer)
[LINQ to SQL tools w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md) obsługuje dziedziczenie pojedynczej tabeli, ponieważ jest on zwykle implementowany w systemach relacyjnych. W tym przewodniku rozszerza ogólne kroki podane w [porady: Konfigurowanie dziedziczenia za pomocą Projektanta obiektów relacyjnych](../data-tools/how-to-configure-inheritance-by-using-the-o-r-designer.md) tematu i zawiera dane rzeczywiste, aby zademonstrować użycie dziedziczenie w [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)].

 Z tego instruktażu należy wykonać następujące zadania:

- Utwórz tabelę bazy danych i Dodaj do niego dane.

- Tworzenie aplikacji Windows Forms.

- Dodaj [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] plik do projektu.

- Tworzenie nowych klas jednostek.

- Konfigurowanie do używania dziedziczenia klas jednostek.

- Zapytania odziedziczoną klasę.

- Wyświetlanie danych w formularzu Windows.

## <a name="create-a-table-to-inherit-from"></a>Utwórz tabelę odziedziczone po
 Aby zobaczyć, jak działa dziedziczenie, należy utworzyć małą `Person` tabeli, użyj go jako klasę bazową, a następnie utwórz `Employee` obiektu, który dziedziczy z niego.

### <a name="to-create-a-base-table-to-demonstrate-inheritance"></a>Do utworzenia tabeli podstawowej, aby zademonstrować dziedziczenia

1.  W **Eksploratora serwera** lub **Eksplorator bazy danych**, kliknij prawym przyciskiem myszy **tabel** węzła i kliknij przycisk **Dodaj nową tabelę**.

    > [!NOTE]
    >  Można użyć bazy danych Northwind lub innej bazy danych można dodać do tabeli.

2.  W **projektanta tabel**, Dodaj następujące kolumny w tabeli:

    |Nazwa kolumny|Typ danych|Zezwalaj na wartości null|
    |-----------------|---------------|-----------------|
    |**ID**|**int**|**False**|
    |**Typ**|**int**|**True**|
    |**Imię**|**Nvarchar(200)**|**False**|
    |**Nazwisko**|**Nvarchar(200)**|**False**|
    |**Menedżer**|**int**|**True**|

3.  Jako klucz podstawowy, należy ustawić kolumny Identyfikatora.

4.  Zapisz tabelę i nadaj mu nazwę **osoby**.

## <a name="add-data-to-the-table"></a>Dodawanie danych do tabeli
 Aby mogli zweryfikować, że dziedziczenie jest prawidłowo skonfigurowany, tabela musi niektóre dane dla każdej klasy w dziedziczeniu pojedynczej tabeli.

### <a name="to-add-data-to-the-table"></a>Aby dodać dane do tabeli

1.  Otwórz tabelę w widoku danych. (Kliknij prawym przyciskiem myszy **osoby** tabelę **Eksploratora serwera** lub **Eksplorator bazy danych** i kliknij przycisk **Pokaż dane tabeli**.)

2.  Skopiuj następujące dane do tabeli. (Można go skopiować i następnie wkleić je do tabeli, wybierając cały wiersz w **wyniki** okienka.)

    ||||||
    |-|-|-|-|-|
    |**ID**|**Typ**|**Imię**|**Nazwisko**|**Menedżer**|
    |**1**|**1**|**Anna**|**Wallace**|**NULL**|
    |**2**|**1**|**Carlos**|**Grilo**|**NULL**|
    |**3**|**1**|**Yael**|**Peled**|**NULL**|
    |**4**|**2**|**Gatis**|**Ozolins**|**1**|
    |**5**|**2**|**Andreas**|**Hauser**|**1**|
    |**6**|**2**|**Tiffany**|**Phuvasate**|**1**|
    |**7**|**2**|**ALEXEY**|**Orekhov**|**2**|
    |**8**|**2**|**Michał**|**Poliszkiewicz**|**2**|
    |**9**|**2**|**Akończenie**|**Yee**|**2**|
    |**10**|**2**|**Fabricio**|**Noriega**|**3**|
    |**11**|**2**|**Beata**|**Martin**|**3**|
    |**12**|**2**|**Krzysztof**|**Kwok**|**3**|

## <a name="create-a-new-project"></a>Tworzenie nowego projektu
 Teraz, po utworzeniu tabeli, należy utworzyć nowy projekt, aby zademonstrować Konfigurowanie dziedziczenia.

### <a name="to-create-the-new-windows-forms-application"></a>Aby utworzyć nową aplikację Windows Forms

1. W programie Visual Studio na **pliku** menu, wybierz opcję **New** > **projektu**.

2. Rozwiń **Visual C#** lub **języka Visual Basic** w okienku po lewej stronie, a następnie zaznacz **pulpitu Windows**.

3. W środkowym okienku wybierz **Windows Forms App** typ projektu.

4. Nadaj projektowi nazwę **InheritanceWalkthrough**, a następnie wybierz **OK**.

     **InheritanceWalkthrough** projekt zostanie utworzony i dodany do **Eksploratora rozwiązań**.

## <a name="add-a-linq-to-sql-classes-file-to-the-project"></a>Dodaj LINQ do SQL plik klasy do projektu

### <a name="to-add-a-linq-to-sql-file-to-the-project"></a>Aby dodać LINQ do SQL pliku do projektu

1.  Na **projektu** menu, kliknij przycisk **Dodaj nowy element**.

2.  Kliknij przycisk **klasy LINQ do SQL** szablonu, a następnie kliknij przycisk **Dodaj**.

     *Dbml* plik zostanie dodany do projektu i **O/R Designer** zostanie otwarty.

## <a name="create-the-inheritance-by-using-the-or-designer"></a>Tworzenie dziedziczenia za pomocą Projektanta obiektów relacyjnych
 Konfigurowanie dziedziczenia, przeciągając **dziedziczenia** obiektu z **przybornika** na powierzchnię projektu.

### <a name="to-create-the-inheritance"></a>Aby utworzyć dziedziczenia

1.  W **Eksploratora serwera** lub **Eksplorator bazy danych**, przejdź do **osoby** tabelę, która została utworzona wcześniej.

2.  Przeciągnij **osoby** tabeli na **O/R Designer** powierzchni projektowej.

3.  Przeciągnij sekundy **osoby** tabeli na **O/R Designer** i zmień jego nazwę na **pracowników**.

4.  Usuń **Menedżera** właściwość **osoby** obiektu.

5.  Usuń **typu**, **identyfikator**, **FirstName**, i **LastName** właściwości z **pracowników** obiektu. (Innymi słowy, Usuń wszystkie właściwości, z wyjątkiem **Menedżera**.)

6.  Z **Object Relational Designer** karcie **przybornika**, Utwórz **dziedziczenia** między **osoby** i  **Pracownik** obiektów. Aby to zrobić, kliknij przycisk **dziedziczenia** pozycja **przybornika** i zwolnij przycisk myszy. Następnie kliknij przycisk **pracowników** obiektu a następnie **osoby** obiektu **O/R Designer**. Następnie wskazuje symbolu strzałki na linii dziedziczenia **osoby** obiektu.

7.  Kliknij przycisk **dziedziczenia** linia na powierzchni projektowej.

8.  Ustaw **właściwość rozróżniacza** właściwości **typu**.

9. Ustaw **wartość dyskryminatora klasy pochodnej** właściwości **2**.

10. Ustaw **wartość dyskryminatora klasy podstawowej** właściwości **1**.

11. Ustaw **domyślne dziedziczenie** właściwości **osoby**.

12. Skompiluj projekt.

## <a name="query-the-inherited-class-and-display-the-data-on-the-form"></a>Zapytanie odziedziczoną klasę i wyświetlić dane w formularzu
 Teraz dodasz kod do formularza, który odpytuje dla określonej klasy w modelu obiektów.

### <a name="to-create-a-linq-query-and-display-the-results-on-the-form"></a>Aby utworzyć zapytanie LINQ i wyświetlić wyniki na formularzu

1.  Przeciągnij **ListBox** na **Form1**.

2.  Kliknij dwukrotnie formularz, aby utworzyć `Form1_Load` programu obsługi zdarzeń.

3.  Dodaj następujący kod do `Form1_Load` program obsługi zdarzeń:

    ```vb
    Dim dc As New DataClasses1DataContext
    Dim results = From emp In dc.Persons _
        Where TypeOf emp Is Employee _
        Select emp

    For Each Emp As Employee In results
        ListBox1.Items.Add(Emp.LastName)
    Next
    ```

    ```csharp
    NorthwindDataContext dc = new DataClasses1DataContext();
    var results = from emp in dc.Persons
                  where emp is Employee
                  select emp;

    foreach(Employee Emp in results)
    {
        listBox1.Items.Add(Emp.LastName)
    }
    ```

## <a name="test-the-application"></a>Testowanie aplikacji
 Uruchom aplikację i sprawdź, czy rekordy wyświetlana w polu listy są wszyscy pracownicy (rekordy, które mają wartość 2 w ich **typu** kolumny).

### <a name="to-test-the-application"></a>Aby przetestować aplikację

1.  Naciśnij klawisz **F5**.

2.  Sprawdź, że tylko rekordy, które mają wartość 2 w ich **typu** kolumny są wyświetlane.

3.  Zamknij formularz. (Na **debugowania** menu, kliknij przycisk **Zatrzymaj debugowanie**.)

## <a name="see-also"></a>Zobacz także

- [Narzędzi LINQ to SQL w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [Wskazówki: Tworzenie LINQ do klas SQL (Projektant O-R)](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [Instrukcje: przypisywanie procedur składowanych na potrzeby wykonywania aktualizacji, wstawiania i usuwania (O/R Designer)](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [Porady: Generowanie modelu obiektu w języku Visual Basic lub C#](/dotnet/framework/data/adonet/sql/linq/how-to-generate-the-object-model-in-visual-basic-or-csharp)