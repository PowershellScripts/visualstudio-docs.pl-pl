---
title: 'Porady: zmiana zwracanego typu metody DataContext (Projektant O-R) | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c5b66bff-6dbb-43c0-bffa-317133ca5b9e
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: e4999c9fd273b78ff740e53c25bbe5a4b0a3017f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49211747"
---
# <a name="how-to-change-the-return-type-of-a-datacontext-method-or-designer"></a>Porady: zmiana zwracanego typu metody DataContext (O/R Designer)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Zwracany typ <xref:System.Data.Linq.DataContext> — metoda (utworzonym w zależności od procedury składowanej lub funkcji) różni się w zależności od tego, gdzie porzucić procedury składowanej lub funkcji w elemencie [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)]. Jeśli usuniesz element bezpośrednio na istniejącej klasy jednostki, <xref:System.Data.Linq.DataContext> metodę, która ma typ zwracany klasy jednostki jest tworzony (Jeśli schemat danych zwróconych przez procedurę składowaną lub funkcję odpowiada kształt klasy jednostek). Jeśli usuniesz element na pustym obszarem [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)], <xref:System.Data.Linq.DataContext> metodę, która zwraca automatycznie wygenerowany typ zostanie utworzony. Możesz zmienić typ zwracany <xref:System.Data.Linq.DataContext> metoda po dodaniu do okienka metod. Aby sprawdzić lub zmienić typ zwracany <xref:System.Data.Linq.DataContext> metody, zaznacz go i kliknij **typie zwracanym** właściwość **właściwości** okna.  
  
> [!NOTE]
>  Nie można cofnąć <xref:System.Data.Linq.DataContext> metody, które mają typ zwracany po ustawieniu klasę jednostki Zwróć typ wygenerowany automatycznie za pomocą **właściwości** okna. Aby przywrócić <xref:System.Data.Linq.DataContext> metodę, aby zwracać typ wygenerowany automatycznie oryginalnego obiektu bazy danych do Projektanta obiektów relacyjnych należy przeciągnąć ponownie.  
  
 [!INCLUDE[note_settings_general](../includes/note-settings-general-md.md)]  
  
### <a name="to-change-the-return-type-of-a-datacontext-method-from-the-auto-generated-type-to-an-entity-class"></a>Zmiany zwracanego typu metody DataContext ze typu automatycznie wygenerowana klasa jednostki  
  
1.  Wybierz <xref:System.Data.Linq.DataContext> metody w okienko metod.  
  
2.  Wybierz **typie zwracanym** w **właściwości** okna, a następnie wybierz jednostki dostępne klasy w **typie zwracanym** listy. Jeśli klasa odpowiedniej jednostki nie jest na liście, dodaj go do, lub utwórz go w [!INCLUDE[vs_ordesigner_short](../includes/vs-ordesigner-short-md.md)] ją dodać do listy.  
  
3.  Zapisz plik dbml.  
  
### <a name="to-change-the-return-type-of-a-datacontext-method-from-an-entity-class-back-to-the-auto-generated-type"></a>Aby zmienić typ zwracany metody DataContext z klasy jednostki na typ wygenerowany automatycznie  
  
1.  Wybierz <xref:System.Data.Linq.DataContext> metody w okienko metod i usuń go.  
  
2.  Przeciągnij obiekt bazy danych z **Eksploratora serwera**/**Eksplorator bazy danych** nad pustym obszarem projektanta O/R.  
  
3.  Zapisz plik dbml.  
  
## <a name="see-also"></a>Zobacz też  
 [LINQ to SQL Tools w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [LINQ do SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)   
 [Metody DataContext (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md)   
 [Instrukcje: tworzenie metod DataContext zamapowanych na procedury składowane i funkcje (O/R Designer)](../data-tools/how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-o-r-designer.md)

