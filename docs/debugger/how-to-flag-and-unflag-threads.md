---
title: 'Porady: Oflagowanie i usuwanie oflagowania wątków | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- treads, switching [debugging]
ms.assetid: 952d579d-6911-413e-b3e5-54e7e797e70c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 09d26c87867e071b7dafce80d95e4bc46cb88bb8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49891378"
---
# <a name="how-to-flag-and-unflag-threads"></a>Porada: Oflagowanie i usuwanie oflagowania wątków
Można flagę wątku, który chcesz poświęcić szczególną uwagę, oznaczając je za pomocą ikony w **wątków**, **stosów równoległych** (Widok wątku) **równoległego wyrażenia kontrolnego**i  **Wątki GPU** systemu windows. Ta ikona może pomóc i inne odróżnić oflagowane wątki z innych wątków.  
  
Oflagowane wątki otrzymają specjalnego traktowania w **wątku** listy na **Lokalizacja debugowania** narzędzi i w innych wielowątkowe debugowanie systemu windows. Możesz wyświetlić wszystkie wątki lub tylko oflagowane wątki w **wątku** listy lub w innych oknach.
  
### <a name="to-flag-or-unflag-a-thread"></a>Flaga lub usuń flagę wątku 
  
- W **wątków** lub **równoległego wyrażenia kontrolnego** oknie Znajdź wątek Cię interesuje i kliknij ikonę flagi, aby zaznacz lub Wyczyść flagę. 
- W **stosów równoległych** okna, kliknij prawym przyciskiem myszy na wątku lub grupy wątków, a następnie wybierz pozycję **flagi / <thread>**  lub **Unflag / <thread>** .
  
### <a name="to-unflag-all-threads"></a>Aby Usuń flagę ze wszystkich wątków  
  
-   W **wątków** okna, kliknij prawym przyciskiem myszy dowolnego wątku, a następnie kliknij przycisk **Usuń flagę ze wszystkich wątków**.
-   W **równoległego wyrażenia kontrolnego** wybierz wszystkie oflagowane wątki, a następnie kliknij prawym przyciskiem myszy i wybierz **Unflag**.  
  
### <a name="to-display-only-flagged-threads"></a>Aby wyświetlić tylko oflagowane wątki  
  
-   Wybierz **Pokaż wątki tylko oflagowane** przycisk w jedną z wielowątkowych debugowania systemu windows.  
  
### <a name="to-flag-just-my-code"></a>Flagi tylko mój kod  
  
1.  Na pasku narzędzi u góry **wątków** okna, kliknij ikonę flagi.  
  
2.  Na liście rozwijanej kliknij **flagę tylko mój kod**.  
  
### <a name="to-flag-threads-that-are-associated-with-selected-modules"></a>Aby Oflaguj wątki, które są skojarzone z wybranych modułów  
  
1.  Na pasku narzędzi **wątków** okna, kliknij ikonę flagi.  
  
2.  Na liście rozwijanej kliknij **Oflaguj niestandardowy wybór modułów**.  
  
3.  W **wybierz moduły** okna dialogowego Wybierz moduły, które chcesz.  
  
4.  (Opcjonalnie) W **wyszukiwania** wpisz ciąg do wyszukiwania określonych modułów.  
  
5.  Kliknij przycisk **OK**.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie aplikacji wielowątkowych](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Rozpoczynanie debugowania aplikacji wielowątkowych](../debugger/get-started-debugging-multithreaded-apps.md)  
 [Przewodnik: Debugowanie aplikacji wielowątkowych, za pomocą okna wątków](../debugger/how-to-use-the-threads-window.md)