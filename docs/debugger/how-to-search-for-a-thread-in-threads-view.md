---
title: 'Porady: wyszukiwanie wątku w widoku wątków | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- threads, searching
ms.assetid: 5609a9b3-c279-4426-9e2e-dd87896a6d6f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 58e16d0edce411192f7b6e40bd0e5fedb32bfac5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49880575"
---
# <a name="how-to-search-for-a-thread-in-threads-view"></a>Porady: wyszukiwanie wątku w widoku wątków
Możesz wyszukać określonego wątku w widoku wątków, za pomocą ciągu Identyfikatora lub moduł jego wątku jako kryterium wyszukiwania. Można również określić początkową kierunek wyszukiwania. Pola w oknie dialogowym pokaże atrybuty zaznaczonych wątków w drzewie wątku.  
  
### <a name="to-search-for-a-thread-in-threads-view"></a>Wyszukiwanie wątku w widoku wątków  
  
1. Rozmieść aplikacji dla systemu windows, więc tego programu Spy ++ i aktywne [Widok wątków](../debugger/threads-view.md) okna są widoczne.  
  
2. Z **wyszukiwania** menu, wybierz **Znajdź wątek**.  
  
    [Okno dialogowe Wyszukiwanie wątków](../debugger/thread-search-dialog-box.md) zostanie otwarty.  
  
3. Wpisz identyfikator wątku lub ciąg modułu jako kryterium wyszukiwania.  
  
4. Wyczyść wszystkie pola, dla których nie chcesz określać wartości.  
  
   > [!TIP]
   >  Aby znaleźć wszystkie wątki, które są własnością modułu, należy wyczyścić **wątku** pole tekstowe i wpisz moduł nazwy **modułu** pole. Następnie użyj **Znajdź następny** kontynuować wyszukiwanie wątków.  
  
5. Wybierz **się** lub **dół** dla początkowej kierunek wyszukiwania.  
  
6. Kliknij przycisk **OK**.  
  
   Jeśli zostanie znalezione pasujące wątku, jest wyróżniona w oknie Widok wątków.