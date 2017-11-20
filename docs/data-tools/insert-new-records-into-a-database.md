---
title: "Wstawianie nowych rekordów do bazy danych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- TableAdapters, inserting new records into
- data [Visual Studio], saving
- databases, inserting new records into
- records, inserting
- saving data
ms.assetid: ea118fff-69b1-4675-b79a-e33374377f04
caps.latest.revision: "11"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 2450ed950227b6755b57f20f3520a1e75034aafe
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="insert-new-records-into-a-database"></a>Wstawianie nowych rekordów do bazy danych
Aby wstawianie nowych rekordów do bazy danych, można użyć `TableAdapter.Update` metody lub jeden element TableAdapter DBDirect — metody (w szczególności `TableAdapter.Insert` metody). Aby uzyskać więcej informacji, zobacz [TableAdapter](../data-tools/create-and-configure-tableadapters.md).  
  
 Jeśli aplikacja nie używa TableAdapters, można użyć polecenia obiektów (na przykład <xref:System.Data.SqlClient.SqlCommand>) do wstawianie nowych rekordów w bazie danych.
  
 Jeśli aplikacja używa zestawów danych do przechowywania danych, użyj `TableAdapter.Update` metody. `Update` Metoda wysyła wszystkie zmiany (aktualizacje, wstawienia i usunięcia) w bazie danych.  
  
 Jeśli aplikacja używa obiektów do przechowywania danych, lub jeśli chcesz bardziej precyzyjną kontrolę nad tworzeniem nowych rekordów w bazie danych, użyj `TableAdapter.Insert` metody.  
  
 Jeśli Twoje TableAdapter nie ma `Insert` metody, oznacza to, że albo TableAdapter jest skonfigurowana do używania procedur składowanych lub jego `GenerateDBDirectMethods` właściwość jest ustawiona na `false`. Spróbuj ustawić element TableAdapter `GenerateDBDirectMethods` właściwości `true` z poziomu **Projektant obiektów Dataset**, a następnie Zapisz zestaw danych. Spowoduje to ponowne wygenerowanie TableAdapter. Jeśli TableAdapter nie ma `Insert` metody, a następnie tabeli prawdopodobnie nie ma wystarczającej ilości informacji o schemacie, aby odróżnić poszczególnych wierszy (na przykład nie może być nie podstawowego klucza ustawiony w tabeli).  
  
## <a name="insert-new-records-by-using-tableadapters"></a>Wstawianie nowych rekordów przy użyciu TableAdapters  
 TableAdapters udostępniają różne sposoby wstawianie nowych rekordów do bazy danych, w zależności od wymagań aplikacji.  
  
 Jeśli aplikacja korzysta z zestawów danych do przechowywania danych, a następnie po prostu dodaniem nowych rekordów do żądaną <xref:System.Data.DataTable> w zestawie danych, a następnie wywołania `TableAdapter.Update` metody. `TableAdapter.Update` Metoda wysyła wszelkie zmiany <xref:System.Data.DataTable> do bazy danych (w tym zmodyfikowane i usuniętych rekordów).  
  
#### <a name="to-insert-new-records-into-a-database-by-using-the-tableadapterupdate-method"></a>Wstawianie nowych rekordów do bazy danych za pomocą TableAdapter.Update — metoda  
  
1.  Dodawanie nowych rekordów do żądaną <xref:System.Data.DataTable> przez utworzenie nowej <xref:System.Data.DataRow> i dodać go do <xref:System.Data.DataTable.Rows%2A> kolekcji. 
  
2.  Po dodaniu nowych wierszy do <xref:System.Data.DataTable>, wywołaj `TableAdapter.Update` metody. Można kontrolować ilość danych do zaktualizowania przez przekazanie w jednym cały <xref:System.Data.DataSet>, <xref:System.Data.DataTable>, tablicę <xref:System.Data.DataRow>s lub pojedynczych <xref:System.Data.DataRow>.  
  
 Poniższy kod przedstawia sposób dodawania nowego rekordu do <xref:System.Data.DataTable> , a następnie wywołać `TableAdapter.Update` metodę, aby zapisać nowy wiersz w bazie danych. (W tym przykładzie użyto `Region` tabeli w bazie danych Northwind.)  
  
 [!code-vb[VbRaddataSaving#14](../data-tools/codesnippet/VisualBasic/insert-new-records-into-a-database_1.vb)]
 [!code-csharp[VbRaddataSaving#14](../data-tools/codesnippet/CSharp/insert-new-records-into-a-database_1.cs)]  
  
#### <a name="to-insert-new-records-into-a-database-by-using-the-tableadapterinsert-method"></a>Wstawianie nowych rekordów do bazy danych za pomocą TableAdapter.Insert — metoda  
Jeśli aplikacja używa obiektów do przechowywania danych, możesz użyć `TableAdapter.Insert` metodę w celu utworzenia nowych wierszy bezpośrednio w bazie danych. `Insert` Metoda przyjmuje poszczególne wartości dla każdej kolumny jako parametry. Wywołanie metody Wstawia nowy rekord w bazie danych przy użyciu wartości parametrów przekazane.  
  
- Wywołaj element TableAdapter `Insert` metody przekazywanie wartości dla każdej kolumny jako parametrów.  

 W poniższej procedurze przedstawiono przy użyciu `TableAdapter.Insert` metodę, aby wstawić wierszy. W tym przykładzie wstawia dane do `Region` tabeli w bazie danych Northwind.  
  
 > [!NOTE]
 >  Jeśli nie masz wystąpienie, które są dostępne, można utworzyć wystąpienia TableAdapter, którego chcesz użyć.  
  
 [!code-vb[VbRaddataSaving#15](../data-tools/codesnippet/VisualBasic/insert-new-records-into-a-database_2.vb)]
 [!code-csharp[VbRaddataSaving#15](../data-tools/codesnippet/CSharp/insert-new-records-into-a-database_2.cs)]  
  
## <a name="insert-new-records-by-using-command-objects"></a>Wstawianie nowych rekordów przy użyciu obiektów poleceń  
Możesz wstawić nowych rekordów bezpośrednio do bazy danych przy użyciu polecenia obiektów.    
  
#### <a name="to-insert-new-records-into-a-database-by-using-command-objects"></a>Wstawianie nowych rekordów do bazy danych za pomocą obiektów poleceń  
  
-   Utwórz nowy obiekt polecenia, a następnie ustaw jego `Connection`, `CommandType`, i `CommandText` właściwości.  

 W poniższym przykładzie pokazano Wstawianie rekordów do bazy danych przy użyciu obiektu polecenia. Wstawia dane do `Region` tabeli w bazie danych Northwind.
  
 [!code-vb[VbRaddataSaving#16](../data-tools/codesnippet/VisualBasic/insert-new-records-into-a-database_3.vb)]
 [!code-csharp[VbRaddataSaving#16](../data-tools/codesnippet/CSharp/insert-new-records-into-a-database_3.cs)]  
  
## <a name="net-framework-security"></a>Zabezpieczenia.NET Framework  
 Musi mieć dostęp do bazy danych, z którym próbujesz nawiązać połączenie, a także uprawnienia do wykonywania operacji wstawiania do żądanej tabeli.  
  
## <a name="see-also"></a>Zobacz też  
 [Zapisywanie danych w bazie danych](../data-tools/save-data-back-to-the-database.md)