---
title: "Porady: przełączanie na inny wątek podczas debugowania | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 04/27/2017
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
helpviewer_keywords: threads, switching [debugging]
ms.assetid: 5cd76c52-76fa-4fcc-b37e-e9f0ecac0e9e
caps.latest.revision: "26"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 14432de4519ed49292810af5f96399bbf87e43cd
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-switch-to-another-thread-while-debugging-in-visual-studio"></a>Porady: przełączanie na inny wątek podczas debugowania w programie Visual Studio
Podczas debugowania aplikacji wielowątkowych służy jednej z kilku metod przejść z wątku, który pracy z do innego wątku.

> [!NOTE]
> Jeśli chcesz kontrolować kolejność, w którym wykonywanie wątków, musisz [zablokować i odblokować wątków](/debugger/get-started-debugging-multithreaded-apps.md).

Po sprawdzeniu wątków w edytorze kodu i oknach debugowania wielowątkowe żółta strzałka wskazuje bieżący wątek. Zielona strzałka z nawiasy tail oznacza, że wątek długoterminowe ma bieżącego kontekstu debugera.
  
### <a name="to-switch-to-any-thread-that-appears"></a>Aby przełączyć się do dowolnego wątku, który pojawi się 
  
-   W **wątków** lub **czujki równoległej** okna, kliknij dwukrotnie wątek.  
  
### <a name="to-switch-to-a-thread-in-a-source-window"></a>Aby przełączyć się do wątku w oknie źródła  
  
-   W odstępu po lewej stronie, kliknij prawym przyciskiem myszy ikonę znacznika wątku ![znacznika wątku](../debugger/media/dbg-thread-marker.png "ThreadMarker"), wskaż **przełączyć się do**, a następnie kliknij nazwę tego wątku, do której chcesz przełączyć . Menu skrótów pokazuje wątki w określonej lokalizacji.  
  
     Jeśli zostanie wyświetlony bez znaczników wątku, kliknij prawym przyciskiem myszy w **wątków** okna i sprawdź, czy **Pokaż wątki w źródle** jest zaznaczone.  
  
### <a name="to-switch-to-a-thread-in-the-debug-location-toolbar"></a>Aby przełączyć się do wątku w pasku narzędzi debugowania lokalizacji  
  
1.  Na **debugowania lokalizacji** narzędzi, kliknij przycisk **wątku** listy.  
  
2.  Na liście kliknij wątek, do której chcesz przełączyć.  
  
## <a name="see-also"></a>Zobacz też  
 [Debuguj aplikacje wielowątkowe](../debugger/debug-multithreaded-applications-in-visual-studio.md)