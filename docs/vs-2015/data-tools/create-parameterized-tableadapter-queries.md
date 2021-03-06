---
title: Tworzenie sparametryzowanych zapytań adaptera TableAdapter | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- data [Visual Studio], TableAdapters
- TableAdapters, parameterized queries
- data [Visual Studio], searching data
- queries [Visual Studio], creating
- TableAdapters, searching data
- queries [Visual Studio], TableAdapters
ms.assetid: 104d1d19-b5a9-4071-b81e-1b3af08e9c7b
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 56e14d66275bd961829fc09e06f7d5e99dbcc2c4
ms.sourcegitcommit: d462dd10746624ad139f1db04edd501e7737d51e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/29/2018
ms.locfileid: "50218902"
---
# <a name="create-parameterized-tableadapter-queries"></a>Tworzenie sparametryzowanych zapytań adaptera TableAdapter
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Uruchamianie zapytania parametrycznego zwraca dane spełniające warunki klauzuli WHERE w ramach zapytania. Na przykład można zdefiniować parametry listę klientów, aby wyświetlić tylko klienci niektóre miasta, dodając `WHERE City = @City` do końca instrukcji SQL, które zwraca listę klientów.  
  
 Tworzenie sparametryzowanych zapytań adaptera TableAdapter w [Projektanta obiektów Dataset](../data-tools/creating-and-editing-typed-datasets.md). Można też utworzyć w aplikacji Windows, za pomocą **parametryzacja źródła danych** polecenie **danych** menu. **Parametryzacja źródła danych** polecenie tworzy formantów w formularzu, gdzie wartości parametrów wejściowych i uruchom zapytanie.  
  
> [!NOTE]
>  Podczas tworzenia zapytania parametrycznego, użyj notacji parametru, które są specyficzne dla bazy danych, która jest kodowania dla. Na przykład źródła danych programu Access i OleDb użyć znaku zapytania '?' do oznaczania parametrów, dlatego klauzuli WHERE będzie wyglądać następująco: `WHERE City = ?`.  
  
> [!NOTE]
>  Polecenia menu i okien dialogowych mogą różnić się od tych opisanych w pomocy, w zależności od Twojego ustawień aktywnych lub wydania, którego używasz. Aby zmienić swoje ustawienia, przejdź do **narzędzia** menu, a następnie wybierz **Import i eksport ustawień**. Aby uzyskać więcej informacji, zobacz [Dostosowywanie ustawień środowiska deweloperskiego, w programie Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## <a name="create-a-parameterized-tableadapter-query"></a>Tworzenie sparametryzowanych zapytań TableAdapter  
  
#### <a name="to-create-a-parameterized-query-in-the-dataset-designer"></a>Aby utworzyć zapytanie parametryczne w Projektancie obiektów Dataset  
  
-   Utwórz nowy obiekt TableAdapter, dodając klauzulę WHERE z odpowiednie parametry do instrukcji SQL. Aby uzyskać więcej informacji, zobacz [tworzenie i konfigurowanie adapterów TableAdapter](../data-tools/create-and-configure-tableadapters.md).  
  
     —lub—  
  
-   Dodaj zapytanie na istniejący obiekt TableAdapter, dodając klauzulę WHERE z odpowiednie parametry do instrukcji SQL. Aby uzyskać więcej informacji, zobacz [porady: tworzenie zapytań TableAdapter](../data-tools/how-to-create-tableadapter-queries.md).  
  
#### <a name="to-create-a-parameterized-query-while-designing-a-data-bound-form"></a>Aby utworzyć zapytanie parametryczne podczas projektowania formularza powiązanych z danymi  
  
1.  Wybierz kontrolkę w formularzu, która jest już powiązany z zestawem danych. Aby uzyskać więcej informacji, zobacz [formanty powiązania formularzy Windows do danych w programie Visual Studio](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md).  
  
2.  Na **danych** menu, wybierz opcję**Dodaj zapytanie**.  
  
3.  Wykonaj **Konstruktor kryteriów wyszukiwania** okno dialogowe, dodając klauzulę WHERE z odpowiednie parametry do instrukcji SQL.  
  
### <a name="to-add-a-query-to-an-existing-data-bound-form"></a>Aby dodać zapytanie do istniejącego formularza powiązanych z danymi  
  
1. Otwórz formularz w **Windows Forms Designer**.  
  
2. Na **danych** menu, wybierz opcję **Dodaj zapytanie** lub **tagów inteligentnych danych**.  
  
   > [!NOTE]
   > Jeśli **Dodaj zapytanie** nie jest dostępny na **danych** menu, wybierz formant w formularzu, wyświetla źródła danych, możesz chcesz dodać parametry do. Na przykład, jeśli w formularzu są wyświetlane dane w <xref:System.Windows.Forms.DataGridView> sterowania, wybierz ją. Jeśli w formularzu wyświetlane dane w poszczególnych formantów, wybierz dowolny formant powiązany z danymi.  
  
3. W **tabeli źródła danych wybierz** obszaru, wybierz tablethat, którą chcesz dodać parametryzacji do.  
  
4. Wpisz nazwę w **Nowa nazwa zapytania** pole, jeśli tworzysz nową kwerendę.  
  
    —lub—  
  
    Wybierz zapytanie w **Ejąca nazwa zapytania** pole.  
  
5. W **tekst zapytania** wpisz kwerendę, która przyjmuje parametry.  
  
6. Wybierz **OK**.  
  
    Co formantu, aby parametr wejściowy, a co **obciążenia** przycisk są dodawane do formularza w <xref:System.Windows.Forms.ToolStrip> kontroli.  
  
   Parametry TableAdapter można przypisać wartości null wyszukiwać rekordy, które nie mają żadnej wartości bieżącej. Na przykład, należy wziąć pod uwagę następujące zapytanie, które ma `ShippedDate` parametru w jego `WHERE` klauzuli:  
  
   `SELECT CustomerID, OrderDate, ShippedDate`  
  
   `FROM Orders`  
  
   `WHERE (ShippedDate = @ShippedDate) OR`  
  
   `(ShippedDate IS NULL)`  
  
   Gdyby to zapytanie w metodzie TableAdapter, wysłać zapytanie o wszystkie zamówienia, które nie zostały wydane z następującym kodem:  
  
   [!code-csharp[VbRaddataTableAdapters#8](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataTableAdapters/CS/Form2.cs#8)]
   [!code-vb[VbRaddataTableAdapters#8](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataTableAdapters/VB/Form2.vb#8)]  
  
#### <a name="to-enable-a-query-to-accept-null-values"></a>Aby włączyć zapytanie, aby akceptować wartości null  
  
1.  W **Projektanta obiektów Dataset**, wybierz zapytanie TableAdapter, które wymaga, aby zaakceptować wartości parametru o wartości null.  
  
2.  W **właściwości** wybierz **parametry**. Naciśnij przycisk wielokropka (**...** ) przycisk, aby otworzyć **Edytor kolekcji parametrów**.  
  
3.  Wybierz parametr, który dopuszcza wartości null i ustaw **AllowDbNull** właściwość `true`.  
  
## <a name="see-also"></a>Zobacz też  
 [Wypełnianie zestawów danych za pomocą adapterów TableAdapter](../data-tools/fill-datasets-by-using-tableadapters.md)

