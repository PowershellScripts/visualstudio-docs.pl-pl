---
title: Raport dotyczący znaczników | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.markers
ms.assetid: 829ce099-172e-4c7e-bbd0-578b110c59bd
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2ccb9c11d39d0500eab0698dc2907ab983964753
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49881628"
---
# <a name="markers-report"></a>Raport dotyczący znaczników
Raport dotyczący znaczników Wyświetla listę znaczników w wyświetlany przedział czasu.  Przesuwanie powiększanie lub ukrywanie pasm, może spowodować znaczniki do wyświetlone lub znikają. Raport zawiera informacje o poszczególnych znaczników:  
  
- Czas, kiedy go już się rozpoczął, względem początku śledzenia.  
  
- Czas jego trwania. Czas trwania jest zero dla flag i komunikatów, ponieważ stanowią one natychmiastowe.  
  
- Identyfikator wątku, który ją wygenerowało.  
  
- Dostawca zdarzeń śledzenia dla Windows (ETW), które ją wygenerowało.  
  
- Seria znacznika, w którym został zapisany.  
  
- Kategoria zdarzenia, dla której należy.  
  
- Jej poziom ważności.  
  
- Jego typ (zakres, Flaga lub komunikat).  
  
- Co określa opis wysokiego poziomu  
  
  Wybierz **wyeksportować** przycisk, aby zapisać raport dotyczący znaczników do pliku CSV. Można użyć danych w pliku CSV z innymi aplikacjami lub narzędzia.  
  
> [!NOTE]
>  Raport dotyczący znaczników można wyświetlić 1000 znaczników. Aby wyświetlić wszystkie znaczniki, należy wyeksportować pełny raport do pliku CSV.