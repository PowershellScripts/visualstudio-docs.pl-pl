---
title: "Błąd: Serwer sieci Web nie mógł znaleźć żądanego zasobu | Dokumentacja firmy Microsoft"
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
helpviewer_keywords: debugger, Web application errors
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 782abbf8a5cb30801bbe6041143e031792ff247a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Błąd: serwer sieci Web nie mógł znaleźć żądanego zasobu
Z powodu zagadnienia dotyczące zabezpieczeń usługi IIS zwrócił błąd ogólny.  
  
 Jedną z możliwych przyczyn jest to konfiguracja zabezpieczeń serwera. Usług IIS 6.0 i starszych wersjach używane programu dodatkowego, znany jako URLScan, Filtrowanie żądań podejrzane i nieprawidłowo sformułowany. Usług IIS 7.0 ma taką samą funkcję filtrowania żądań wbudowanych. W obu przypadkach funkcja filtrowania żądań zbyt restrykcyjne uniemożliwia Visual Studio debugowanie serwera.  
  
 Istnieje wiele możliwych przyczyn tego błędu. Kilka najbardziej typowe przyczyny obejmują problem z instalacji usług IIS lub konfiguracji, konfiguracja witryny sieci web lub uprawnień w systemie plików. Możesz spróbować uzyskać dostęp do zasobu w przeglądarce. W zależności od sposobu skonfigurowania usług IIS może być konieczne na serwerze przy użyciu przeglądarki sieci lokalnej lub Sprawdź dziennik błędów programu IIS, aby uzyskać szczegółowy komunikat o błędzie.  
  
 Aby uzyskać więcej informacji na temat usuwania usług IIS, zobacz [zarządzania usługami IIS i administrowanie](http://go.microsoft.com/fwlink/?LinkId=255872).  
  
## <a name="see-also"></a>Zobacz też  
 [Narzędzia zabezpieczeń dotyczące narzędzia UrlScan](http://www.microsoft.com/technet/security/tools/urlscan.mspx)   
 [Błąd: Serwer sieci Web został zablokowany i blokuje zlecenie DEBUG](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)