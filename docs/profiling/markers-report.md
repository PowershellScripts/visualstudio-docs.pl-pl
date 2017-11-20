---
title: "Raport dotyczący znaczników | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
caps.latest.revision: "6"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1d9d546e96d92c26725bc8a169c413bc7b96feb7
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="markers-report"></a>Raport dotyczący znaczników
Raport dotyczący znaczników wymieniono znaczników w wyświetlany przedział czasu.  Przesuwanie powiększanie lub ukrywanie pasm, może spowodować znaczników lub pojawiania się. Raport zawiera informacje o poszczególnych znaczników:  
  
-   Czas, gdy rozpoczęto, względem początku śledzenia.  
  
-   Jego czas trwania. Czas trwania wynosi zero dla flagi i komunikaty, ponieważ stanowią one natychmiastowe.  
  
-   Identyfikator wątku, który wygenerował go.  
  
-   Dostawca zdarzenia śledzenia zdarzeń systemu Windows (ETW), która go wygenerowała.  
  
-   Seria znacznika, w którym został zapisany.  
  
-   Kategoria zdarzenia, które należy do.  
  
-   Jej poziom ważności.  
  
-   Jego typ (zakres, Flaga lub komunikat).  
  
-   Opis wysokiego poziomu co reprezentuje  
  
 Wybierz **wyeksportować** przycisk, aby zapisać raport dotyczący znaczników do pliku CSV. Dane można użyć w pliku CSV z innych aplikacji lub narzędzi.  
  
> [!NOTE]
>  Raport dotyczący znaczników można wyświetlić 1000 znaczników. Aby wyświetlić wszystkie znaczniki, należy wyeksportować pełny raport do pliku CSV.