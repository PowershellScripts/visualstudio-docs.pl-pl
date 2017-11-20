---
title: "Błąd: SQL może &#39; znaleźć SSDEBUGPS | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.error.sqlde_cant_find_ssdebugps
dev_langs:
- CSharp
- VB
- FSharp
- C++
- SQL
ms.assetid: 596425c8-14c7-4c05-8823-e1c52f420f5e
caps.latest.revision: "6"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 43a437cfc4be1c9168b16e4b9d1a46e2eadcb2e6
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="error-sql-can39t-find-ssdebugps"></a>Błąd: SQL może &#39; znaleźć SSDEBUGPS
Biblioteka SSDEBUGPS.dll jest składnikiem hosta debugowanie serwera SQL.  
  
 Ten błąd występuje, gdy chcesz rozpocząć debugowania i wskazuje, że określony plik nie jest obecny w [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] maszyny. Możliwe przyczyny to nigdy nie uruchomiono Instalatora albo zdalnego debugowania, lub że jakiś sposób ten plik został usunięty.  
  
 Istnieją dwa sposoby, aby rozwiązać ten problem: ponownie instalację zdalnego debugowania i przez kopiowanie plików na [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] maszyny.  
  
 Aby ponownie uruchomić Instalatora zdalnego debugowania, postępuj zgodnie z instrukcjami w [zdalnego debugowania](../debugger/remote-debugging.md).  
  
 Jeśli kopia Biblioteka ssdebugps.dll może zlokalizować, możesz skopiować go na [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] maszyny. Jeśli istnieje, plik zostanie w \Program Files\ katalogu wspólnej Files\Microsoft Shared\SQL debugowania. Można go znaleźć na innym [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] komputera, lub na komputerze, na którym ma [!INCLUDE[vsprvslong](../code-quality/includes/vsprvslong_md.md)] zainstalowane.  
  
### <a name="to-copy-ssdebugpsdll-onto-the-sql-server-2005-machine"></a>Aby skopiować Biblioteka SSDEBUGPS.dll na komputerze programu SQL Server 2005  
  
1.  Skopiuj plik do katalogu z taką samą nazwę i ścieżkę na [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] maszyny.  
  
2.  Zarejestruj go przez otwarcie **wiersza polecenia**i uruchom następujące polecenie:  
  
    ```  
    regsrv32 ssdebugps.dll  
    ```