---
title: 'Porady: debugowanie hostowania samoobsługowego WCF usługi | Dokumentacja firmy Microsoft'
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
- debugging, WCF
- WCF, self-hosted service
- WCF, debugging
ms.assetid: 288922be-ba3f-411e-af50-bba39c9529cc
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 255ca0f7d472060d110135536d76de99dc46a18e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49872125"
---
# <a name="how-to-debug-a-self-hosted-wcf-service"></a>Porady: debugowanie hostowania samoobsługowego WCF
A *usługi hosta samodzielnego* to usługa WCF, która nie jest uruchamiane w usługach IIS, Host usługi WCF, lub [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] serwera projektowego. Najprostszym sposobem na debugowanie hostowania samoobsługowego WCF jest skonfigurowanie [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] do uruchomienia klienta i serwera, po wybraniu **Rozpocznij debugowanie** na **debugowania** menu.  
  
 Jeśli usługa WCF jest hostingu samodzielnego wewnątrz, czy Proces, który nie można uruchomić w ten sposób, takich jak usługa NT nie można użyć tej metody. Zamiast tego możesz wykonać jedną z następujących czynności:  
  
-   Ręcznie dołączyć debuger do procesu hostingu. Aby uzyskać więcej informacji, zobacz [dołączenia do uruchamiania procesów](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).  
  
     — lub —  
  
-   Rozpocznij debugowanie klienta, a następnie wejdź do wywołań do usługi. Ta migracja wymaga włączenia debugowania w pliku app.config. Aby uzyskać więcej informacji [ograniczenia debugowania WCF](../debugger/limitations-on-wcf-debugging.md).  
  
### <a name="to-start-both-client-and-host-from-visual-studio"></a>Można uruchomić zarówno klient, jak i hosta w programie Visual Studio  
  
1. Utwórz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] rozwiązania zawierającego projekty zarówno klient, jak i serwera.  
  
2. Konfigurowanie rozwiązania do uruchamiania procesów klienta i serwera, po wybraniu **Start** na **debugowania** menu.  
  
   1.  W **Eksploratora rozwiązań**, kliknij prawym przyciskiem myszy nazwę rozwiązania.  
  
   2.  Kliknij przycisk **Ustaw projekty startowe**.  
  
   3.  W **rozwiązania \<name > właściwości** okno dialogowe, wybierz opcję **wiele projektów startowych**.  
  
   4.  W **wiele projektów startowych** siatki w wierszu, który odnosi się do projektu serwera, kliknij przycisk **akcji** i wybierz polecenie **Start**.  
  
   5.  W wierszu, który odnosi się do projektu klienta, kliknij przycisk **akcji** i wybierz polecenie **Start**.  
  
   6.  Kliknij przycisk **OK**.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie usług WCF](../debugger/debugging-wcf-services.md)   
 [Ograniczenia debugowania WCF](../debugger/limitations-on-wcf-debugging.md)   
 [Instrukcje: przechodzenie do usług WCF](../debugger/how-to-step-into-wcf-services.md)