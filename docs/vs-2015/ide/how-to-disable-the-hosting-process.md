---
title: 'Porady: wyłączanie procesu hostingu | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- hosting process, disabling
- vshost.exe, disabling the hosting process
ms.assetid: 9157488d-737f-454b-8d8d-36f99de38bb0
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4251e5aac5042b610ed32f95a13ba5d6ffb9d4eb
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49848492"
---
# <a name="how-to-disable-the-hosting-process"></a>Porady: wyłączanie procesu hostingu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Wywołania niektórych interfejsów API mogą mieć wpływ na włączenie procesu hostingu. W takich przypadkach zachodzi konieczność wyłączanie procesu hostingu, aby zwracać poprawnych wyników.  
  
### <a name="to-disable-the-hosting-process"></a>Aby wyłączyć procesu hostingu  
  
1. Otwórz projekt wykonywalny w [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Projekty, które nie tworzą pliki wykonywalne (na przykład klasy biblioteki lub usługi projektów) nie ma takiej możliwości.  
  
2. Na **projektu** menu, kliknij przycisk **właściwości**.  
  
3. Kliknij przycisk **debugowania** kartę.  
  
4. Wyczyść **włączyć procesu hostingu Visual Studio** pole wyboru.  
  
   Po wyłączeniu procesu hostingu kilka funkcji debugowania są niedostępne lub wystąpić obniżenie wydajności. Aby uzyskać więcej informacji, zobacz [debugowanie i proces hostingu](../debugger/debugging-and-the-hosting-process.md).  
  
   Ogólnie rzecz biorąc, gdy proces hostingu jest wyłączony:  
  
-   Czas potrzebny, aby rozpocząć debugowanie [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] zwiększa aplikacji.  
  
-   Obliczanie wyrażenia czasu projektowania jest niedostępny.  
  
-   Debugowanie w częściowej relacji zaufania jest niedostępny.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie i proces hostingu](../debugger/debugging-and-the-hosting-process.md)   
 [Proces hostingu (vshost.exe)](../ide/hosting-process-vshost-exe.md)   
 [Kompilacje podczas tworzenia aplikacji](http://msdn.microsoft.com/en-us/c9497d62-3b7b-4449-88e8-cf27acc9efe6)



