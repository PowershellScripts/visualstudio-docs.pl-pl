---
title: 'Błąd: Serwer sieci Web nie może znaleźć żądanego zasobu | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: becdd23fd5351fd02b6dc44bd849b8e627e602bb
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49191702"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Błąd: serwer sieci Web nie mógł znaleźć żądanego zasobu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ze względu na zagadnienia dotyczące zabezpieczeń usługi IIS zwrócił błąd ogólny.  
  
 Jedną z możliwych przyczyn jest konfiguracji zabezpieczeń serwera. Usług IIS 6.0 i starszych wersjach umożliwia programu dodatkowego, znane jako narzędzia URLScan, wyfiltruj żądania, podejrzanych i źle sformułowane. Usługi IIS 7.0 ma wbudowane Filtrowanie żądań, w tym samym celu. W obu przypadkach Filtrowanie żądań zbyt restrykcyjne można zapobiec programu Visual Studio debugowanie serwera.  
  
 Istnieje wiele możliwych przyczyn tego błędu. Kilka najczęstszych przyczyn obejmują problem z instalacji usług IIS lub konfiguracji, konfiguracja witryny sieci web lub uprawnienia w systemie plików. Możesz wypróbować, uzyskiwanie dostępu do zasobów za pomocą przeglądarki. W zależności od sposobu skonfigurowania usług IIS może być konieczne korzystanie z przeglądarki lokalnego na serwerze lub Sprawdź dziennik błędów programu IIS, aby uzyskać szczegółowy komunikat o błędzie.  
  
 Aby uzyskać więcej informacji na temat rozwiązywania problemów usług IIS, zobacz [zarządzania usługami IIS i administrowanie](http://go.microsoft.com/fwlink/?LinkId=255872).  
  
## <a name="see-also"></a>Zobacz też  
 [Narzędzia zabezpieczeń dotyczące narzędzia UrlScan](http://www.microsoft.com/technet/security/tools/urlscan.mspx)   
 [Błąd: Serwer internetowy został zablokowany i blokuje czasownik DEBUG](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)



