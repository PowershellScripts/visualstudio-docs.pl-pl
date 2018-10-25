---
title: 'Błąd: ASP.NET nie jest zainstalowany | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.http_not_supported
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Web applications, errors
- debugger, Web application errors
- error messages, ASP.NET
- ASP.NET, installation error messages
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- aspnet
ms.openlocfilehash: 754d196ba49e97ed0a70ca988d4ae65aed001bdc
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49949581"
---
# <a name="error-aspnet-not-installed"></a>Błąd: ASP.NET nie jest zainstalowany
Ten błąd występuje, gdy [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] nie jest poprawnie zainstalowany na komputerze, który chcesz debugować. Może to oznaczać, że [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] nigdy nie został zainstalowany lub [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] została zainstalowana jako pierwsza i IIS został zainstalowany później.  
  
### <a name="to-reinstall-aspnet"></a>Ponowna instalacja programu ASP.NET  
  
1. Z poziomu okna wiersza polecenia Uruchom następujące polecenie:  
  
   ```cmd
   \WINDOWS\Microsoft.NET\Framework\version\aspnet_regiis -i  
   ```  
  
    gdzie *wersji* reprezentuje numer wersji .NET Framework zainstalowanej na komputerze, na przykład v1.0.370. Można określić framework w wersji, przeszukując `\WINDOWS\Microsoft.NET\Framework` katalogu.  
  
   > [!NOTE]
   >  Windows Server 2003, można zainstalować [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] przy użyciu **apletu Dodaj lub usuń programy** w Panelu sterowania.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie aplikacji internetowych: błędy i rozwiązywanie problemów](../debugger/debugging-web-applications-errors-and-troubleshooting.md)
