---
title: 'Błąd: Serwer sieci Web nie może znaleźć żądanego zasobu | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8769c84237d877f02b7c9d3d02c6391f9e955ff3
ms.sourcegitcommit: 40b6438b5acd7e59337a382c39ec711b9e99cc8a
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/11/2018
ms.locfileid: "49100981"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Błąd: serwer sieci Web nie mógł znaleźć żądanego zasobu
Ze względu na zagadnienia dotyczące zabezpieczeń usługi IIS zwrócił błąd ogólny.  

Jedną z możliwych przyczyn jest konfiguracji zabezpieczeń serwera. Usług IIS 6.0 i starszych wersjach umożliwia programu dodatkowego, znane jako narzędzia URLScan, wyfiltruj żądania, podejrzanych i źle sformułowane. Usługi IIS 7.0 ma wbudowane Filtrowanie żądań, w tym samym celu. W obu przypadkach Filtrowanie żądań zbyt restrykcyjne można zapobiec programu Visual Studio debugowanie serwera.  

Inną możliwą przyczyną tego błędu jest, że nie uruchomiono usługi W3SVC dla usług IIS. Sprawdź, czy ta usługa jest uruchomiona (wygaszone out) w oknie usług (*services.msc*).

Istnieją dodatkowe wiele możliwych przyczyn tego błędu. Kilka najczęstszych przyczyn obejmują problem z instalacji usług IIS lub konfiguracji, konfiguracja witryny sieci web lub uprawnienia w systemie plików. Możesz wypróbować, uzyskiwanie dostępu do zasobów za pomocą przeglądarki. W zależności od sposobu skonfigurowania usług IIS może być konieczne korzystanie z przeglądarki lokalnego na serwerze lub Sprawdź dziennik błędów programu IIS, aby uzyskać szczegółowy komunikat o błędzie.  
  
 Aby uzyskać więcej informacji na temat rozwiązywania problemów usług IIS, zobacz [zarządzania usługami IIS i administrowanie](/iis/manage/provisioning-and-managing-iis/iis-management-and-administration).  
  
## <a name="see-also"></a>Zobacz też  
 [Błąd: Serwer internetowy został zablokowany i blokuje czasownik DEBUG](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)