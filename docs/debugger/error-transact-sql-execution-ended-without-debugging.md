---
title: "Błąd: Wykonanie Transact-SQL zakończyło się bez debugowania | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.error.sqlde_sql_executed_but_not_debugged
dev_langs:
- CSharp
- VB
- FSharp
- C++
- SQL
ms.assetid: 7a4d4999-3973-4339-ba6a-f0d19bcb1d4a
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: db04460c57dd4ade94154fa1a884477452ee4108
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="error-transact-sql-execution-ended-without-debugging"></a>Błąd: Wykonanie Transact-SQL zakończyło się bez debugowania
Ten błąd występuje, gdy chcesz debugować języka Transact-SQL lub procedury SQLCLR i debuger nie odbiera komunikaty debugowania z programu SQL Server.  
  
 Może to być spowodowane problemami z siecią lub problemów w programie SQL Server, ale najbardziej prawdopodobną przyczyną jest problem uprawnień.  
  
 Obejmuje dwa konta:  
  
-   Konto aplikacji jest konto użytkownika, który [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] działa jako.  
  
-   Konto połączenia jest tożsamość użyta do nawiązania połączenia z programem SQL Server. To nie jest zawsze taki sam jak tożsamości, która Visual Studio działa tak, jakby połączenie za pomocą uwierzytelniania SQL.  
  
 Debugowanie SQL wymaga, aby konto aplikacji musi zgodne z kontem połączenia lub być sysadmin.  
  
 Jeśli używasz identyfikatora logowania SQL, takich jak sa, konto aplikacji należy skonfigurować w programie SQL Server jako administratora systemu. Domyślnie administratorów na komputerze serwera SQL jest uruchomiona na są sysadmins programu SQL Server.  
  
 Aby rozwiązać ten problem, może być konieczne:  
  
-   Sprawdź ustawienia uprawnień. Aby uzyskać więcej informacji, zobacz [porady: Ustawianie uprawnień serwera SQL dla debugowania](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
-   Upewnij się, że debugowanie SQL, jeśli są nieprawidłowo skonfigurowane.  
  
-   Zapoznaj się z administratorem sieci lub bazy danych.  
  
## <a name="see-also"></a>Zobacz też  
 [Konfigurowanie debugowania SQL](http://msdn.microsoft.com/en-us/3db09e68-edcc-42de-9c22-4e97cfd55ab3)   
 [Porady: Ustawianie uprawnień programu SQL Server do debugowania](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [Ustawienia debugowania i przygotowanie](../debugger/debugger-settings-and-preparation.md)   
 [Debugowanie zdalne](../debugger/remote-debugging.md)