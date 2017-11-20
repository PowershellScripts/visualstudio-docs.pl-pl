---
title: "Wskazówki dotyczące debugowanie wątków w kodzie natywnym | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], threads
ms.assetid: 0374c8c6-57a3-4cfe-8047-2effef5ff5dc
caps.latest.revision: "22"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9b0a2df03fdcb32e09824e37c26587912c542dea
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="tips-for-debugging-threads-in-native-code"></a>Wskazówki dotyczące debugowanie wątków w kodzie natywnym
Poniżej przedstawiono kilka wskazówek, których można używać podczas debugowanie wątków w kodzie natywnym:  
  
-   Można wyświetlić zawartość blok informacji o wątku, wpisując `@TIB` w **czujki** okna lub **QuickWatch** okno dialogowe.  
  
-   Można wyświetlić kod ostatniego błędu dla bieżącego wątku, wprowadzając `@Err` w **czujki** okna lub **QuickWatch** okno dialogowe.  
  
-   Biblioteki wykonawcze języka C (CRT) funkcje mogą być przydatne w przypadku debugowanie aplikacji wielowątkowych. Aby uzyskać więcej informacji, zobacz [_malloc_dbg —](/cpp/c-runtime-library/reference/malloc-dbg).  
  
## <a name="see-also"></a>Zobacz też  
 [Debuguj aplikacje wielowątkowe](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Debugowanie kodu natywnego](../debugger/debugging-native-code.md)