---
title: 'Porady: Tworzenie raportu śledzenia wywołań narzędzi profilowania | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- performance tools, viewing ETW data
- ETW [Visual Studio ALM], viewing data
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
caps.latest.revision: 24
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6b3d54c0d9c053b8ea35b6f8000135b259f8323a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49251904"
---
# <a name="how-to-create-a-profiling-tools-call-trace-report"></a>Porady: tworzenie raportu śledzenia wywołań narzędzi profilowania
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

*Raport śledzenia wywołań* dla [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Profiling Tools Wyświetla listę informacji chronometrażu dla każdego punktu wejścia i wyjścia do funkcji w aplikacji oraz dla każdego wywołania innych funkcji przez funkcję. Raporty śledzenia wywołań są dostępne dla danych profilowania, tylko wtedy, gdy zostały one pobrane metodą instrumentacji.  
  
> [!NOTE]
>  Nie można wyświetlić raportów śledzenia wywołań w [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Należy użyć **VSPerfReport** narzędzie wiersza polecenia do generowania wartości rozdzielanych przecinkami (.csv) lub plik Xml. Aby uzyskać więcej informacji o tym narzędziu, zobacz [VSPerfReport](../profiling/vsperfreport.md).  
  
### <a name="to-create-a-call-trace-report"></a>Aby utworzyć raport śledzenia wywołań  
  
1.  Otwórz **polecenia**okno.  
  
2.  W wierszu polecenia wpisz następujące polecenie:  
  
     *ToolsPath* **VSPerfReport** *Plik_vsp* **/calltrace [podsumowań w plikach]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|Ścieżka narzędzi wiersza polecenia Profiling Tools. Aby uzyskać więcej informacji, zobacz [Określanie ścieżki do narzędzi wiersza polecenia](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|  
    |*Plik_vsp*|Plik danych profilowania (.vsp lub .vsps). Akceptowane są pełne i częściowe ścieżki.|  
    |Xml|Generuje raport w formacie Xml.|  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: zbieranie zdarzeń śledzenia dla danych Windows (ETW)](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)   
 [Interfejsy API narzędzi profilowania](../profiling/profiling-tools-apis.md)



