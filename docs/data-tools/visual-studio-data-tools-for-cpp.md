---
title: Visual Studio tools danych dla C++ | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 3a3849d9-1bc7-47d1-805e-1755223ccba2
caps.latest.revision: "9"
author: gewarren
ms.author: gewarren
manager: ghogen
robots: noindex,nofollow
ms.technology: vs-data-tools
ms.openlocfilehash: c5952c4ab8e8adac0338d406800a15a8a0b12989
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="visual-studio-data-tools-for-c"></a>Visual Studio tools danych dla języka C++
Natywnych języka C++ często zapewnia największą wydajność, gdy uzyskujesz dostęp do źródła danych. Jednak dane narzędzi dla aplikacji w języku C++ w programie Visual Studio nie jest w głębokiej, podobnie jak w przypadku aplikacji .NET. Na przykład windows źródeł danych nie może służyć do przeciągania i upuszczania źródeł danych na powierzchnię projektu C++. Warstwa obiektów relacyjnych należy należy napisać własny lub użyj innej firmy.  To samo dotyczy funkcji wiązania danych, mimo że aplikacje korzystające z biblioteki Microsoft Foundation klasy można używać niektórych klas baz danych, wraz z dokumentami i widokami, przechowywanie danych w pamięci i wyświetlić je użytkownikowi. Aby uzyskać więcej informacji, zobacz [dostęp do danych w programie Visual C++](https://msdn.microsoft.com/en-us/library/7wtdsdkh.aspx) .  
  
 Aby nawiązać połączenie bazy danych SQL, natywnych aplikacji C++ można użyć sterowników ODBC i OLE DB i dostawcy ADO, które są dołączone do systemu Windows. Te można połączyć się z dowolnej bazy danych, która obsługuje te interfejsy. Sterownik ODBC jest standardowym. OLE DB jest dostępne w celu zgodności z poprzednimi wersjami. Aby uzyskać więcej informacji dotyczących tych technologii danych, zobacz [składniki dostępu do danych systemu Windows](https://msdn.microsoft.com/en-us/library/windows/desktop/aa968814\(v=vs.85\).aspx)  
  
 Aby móc korzystać z funkcji niestandardowych w programie SQL Server 2005 i nowszym, użyj [SQL Server Native Client](https://msdn.microsoft.com/en-us/sqlserver/aa937733). Aplikacja native client zawiera także sterownik ODBC programu SQL Server i SQL Server dostawcy OLE DB w jednej macierzystej dynamicznej biblioteki dołączanej (dynamicznie DLL). Obsługują one aplikacji za pomocą API kodu macierzystego (ODBC, OLE DB i ADO) do programu Microsoft SQL Server.  Instaluje program SQL Server Native Client z programu SQL Server Data Tools. Podręcznik programowania jest tutaj: [programu SQL Server Native klienta programowania](https://msdn.microsoft.com/en-us/library/ms130892.aspx).  
  
## <a name="to-connect-to-localdb-through-odbc-and-sql-native-client-from-a-c-application"></a>Aby nawiązać połączenie localDB za pośrednictwem ODBC i SQL Native Client z poziomu aplikacji w języku C++  
  
1.  Zainstaluj program SQL Server Data Tools.  
  
2.  Przykładowa baza danych SQL do nawiązania połączenia, należy pobrać bazy danych Northwind i Rozpakuj go do nowej lokalizacji.  
  
3.  Umożliwia dołączenie rozpakować pliku Northwind.mdf localDB programu SQL Server Management Studio. Po uruchomieniu programu SQL Server Management Studio połącz się (localdb) \MSSQLLocalDB.  
  
     ![Okno dialogowe Połącz SSMS](../data-tools/media/raddata-ssms-connect-dialog.png "raddata SSMS połączyć z okna dialogowego")  
  
     Kliknij prawym przyciskiem myszy w węźle localdb w okienku po lewej stronie i wybierz polecenie **Attach**.  
  
     ![Dołącz SSMS bazy danych](../data-tools/media/raddata-ssms-attach-database.png "raddata SSMS dołączyć w bazie danych")  
  
4.  Pobierz przykład zestawu SDK systemu Windows ODBC i Rozpakuj go do nowej lokalizacji. W tym przykładzie przedstawiono podstawowe polecenia ODBC, które są używane do połączenia z bazą danych i problem zapytań i poleceń. Dowiedz się więcej o tych funkcji w [Otwórz połączenie bazy danych (ODBC) firmy Microsoft](https://msdn.microsoft.com/en-us/library/windows/desktop/ms710252\(v=vs.85\).aspx). Podczas ładowania najpierw rozwiązania (jest w folderze C++), programu Visual Studio oferuje Uaktualnij rozwiązanie do bieżącej wersji programu Visual Studio. Kliknij przycisk **Tak**.  
  
5.  Aby korzystać z natywnego klienta, należy jego plik nagłówka i pliku lib. Te pliki zawierają funkcje i definicje charakterystyczne dla programu SQL Server poza funkcji ODBC zdefiniowanych w sql.h. W **projektu** > **właściwości** > **katalogi VC ++**, Dodaj katalog dołączania następujące:  
  
 **\<dysk systemowy >: \Program Files\Microsoft SQL Server\110\SDK\Include** i ten katalog biblioteki:  
  
 **c:\Program Files\Microsoft SQL Server\110\SDK\Lib**  
  
6.  Dodaj następujące wiersze w odbcsql.cpp. #Define uniemożliwia kompilowany nie znaczenia definicji OLE DB.  
  
    ```C++  
    #define _SQLNCLI_ODBC_  
    #include <sqlncli.h>  
    ```  
  
     Należy pamiętać, że próbki nie faktycznie funkcjonalności klienta natywnej, poprzednie kroki nie są niezbędne, aby skompilować i uruchomić. Ale projektu jest skonfigurowany do użycia tej funkcji. Aby uzyskać więcej informacji, zobacz [programu SQL Server Native klienta programowania](https://msdn.microsoft.com/en-us/library/ms130892\(v=sql.130\).aspx).  
  
7.  Określ, który sterownik do użycia w podsystemie ODBC. Przykład przekazuje atrybut parametrów połączenia sterownika w jako argument wiersza polecenia. W **projektu** > **właściwości** > **debugowanie**, Dodaj ten argument polecenia:  
  
    ```C++  
    DRIVER="SQL Server Native Client 11.0"  
    ```  
  
8.  Naciśnij klawisz F5, aby skompilować i uruchomić aplikację. Powinny pojawić okno dialogowe w sterowniku wyświetli monit o wprowadzenie bazy danych. Wprowadź `(localdb)\MSSQLLocalDB`i sprawdź **Użyj zaufanego połączenia**. Press **OK**. Powinna zostać wyświetlona konsola z komunikatów, które wskazują udane połączenie. Należy również sprawdzić wiersza polecenia można wpisać w instrukcji SQL. Poniższym ekranie przedstawiono przykładowe zapytanie i wyniki:  
  
     ![Przykładowe ODBC wyniki zapytania](../data-tools/media/raddata-odbc-sample-query-output.png "raddata ODBC przykładowe zapytanie w danych wyjściowych")  
  
## <a name="see-also"></a>Zobacz też  
 [Uzyskiwanie dostępu do danych w programie Visual Studio](../data-tools/accessing-data-in-visual-studio.md)