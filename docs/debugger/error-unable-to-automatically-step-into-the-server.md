---
title: 'Błąd: Nie można automatycznie krok po kroku serwera | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.causality_no_server_response
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, notification error
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 37298dcbb2443755136c4c57eb4633fcb3197a87
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49849518"
---
# <a name="error-unable-to-automatically-step-into-the-server"></a>Błąd: Nie można automatycznie rozpocząć wykonywania krok po kroku na serwerze
Odczytuje błąd:  
  
 Nie można automatycznie krok po kroku do serwera. Debuger nie został powiadomiony, zanim była wykonywana ta procedura zdalnego  
  
 Ten błąd może wystąpić, gdy chcesz wejść do usługi sieci web (zobacz [przechodzenie krok po kroku w usłudze internetowej XML](https://msdn.microsoft.com/library/8e67de38-bf5f-41cc-a457-1b88ce63d764)). Może wystąpić, gdy [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] nie jest skonfigurowany prawidłowo.  
  
 Możliwe przyczyny to:  
  
- Plik web.config dla Twojego [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] aplikacji nie powoduje ustawienia debugowania na wartość "true" (zobacz [tryb debugowania w aplikacjach ASP.NET](../debugger/how-to-enable-debugging-for-aspnet-applications.md)).  
  
- Wersja [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] został zainstalowany po zainstalowaniu programu Visual Studio. [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] powinien zostać zainstalowany przed Visual Studio. Aby rozwiązać ten problem, należy użyć Windows **Panel sterowania > programy i funkcje** naprawić instalację programu Visual Studio.  
  
## <a name="see-also"></a>Zobacz też  
 [Błędy związane z debugowaniem zdalnym i rozwiązywanie problemów](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Debugowanie zdalne](../debugger/remote-debugging.md)