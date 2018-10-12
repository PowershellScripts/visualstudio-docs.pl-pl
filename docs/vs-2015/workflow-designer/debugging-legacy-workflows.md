---
title: Debugowanie starszych wersji przepływów pracy | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- workflows, debugging
- debugging, workflows
- debugging workflows
ms.assetid: e6097b47-760a-4b30-a92c-ae70cdbda49f
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 8e35b16d10bf59b4ae8c91de2a5281d540c0e67c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49210603"
---
# <a name="debugging-legacy-workflows"></a>Debugowanie starszych wersji przepływów pracy
Jeśli używasz starszej wersji [!INCLUDE[wfd1](../includes/wfd1-md.md)] w [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] tworzenie [!INCLUDE[wf](../includes/wf-md.md)] aplikacji czy target.NET Framework 3.0 lub 3.5, można debugować z przepływami pracy, jak każdy inny program ustawiania punktów przerwania, dołączanie do procesów i wątków badanie i stos wywołań. Istnieje również możliwość debugowania zdalnego.  
  
> [!NOTE]
>  Jeśli zostały zainstalowane i odinstalować na komputerze wielu wersji programu Visual Studio, debugowanie WF3 może zakończyć się niepowodzeniem przy użyciu jednego z dwóch następujące możliwości:  
>   
>  -   Nie są osiągane punktów przerwania.  
> -   Zostanie wyświetlony następujący komunikat:  
>   
>  **Nie można rozpocząć debugowania na serwerze sieci web. Debuger nie jest poprawnie zainstalowany.  Nie można debugować żądanego typu kodu.  Uruchom Instalatora, aby zainstalować lub naprawić debuger.**  
>   
>  Jeśli wystąpi jedno z tych scenariuszy podczas debugowania środowiska .NET Framework 3.0 lub 3.5 przepływy pracy, wykonaj naprawę instalacji programu Visual Studio.  
  
 [!INCLUDE[wf2](../includes/wf2-md.md)] integruje się z następujących standardowych [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] debugowania systemu windows:  
  
-   **Punkt przerwania**: działa zgodnie z oczekiwaniami, ale Określ działanie dla nazwy funkcji.  
  
-   **Stos wywołań**: zmodyfikowane w celu zapewnienia zarys czynności, które zostały wykonane w wystąpieniu przepływu pracy. Wpisy w **stos wywołań** są najpierw głębokość wyszukiwania wykonywania działań. Możesz kliknąć dwukrotnie wpis, aby Umieść fokus na wybrane działanie.  
  
-   **Wątki**: zawiera identyfikator wystąpienia wystąpienia przepływu pracy, która jest debugowana.  
  
 Visual Studio dla Windows Workflow Foundation nie obsługuje następujących funkcji debugowania:  
  
-   Warunkowe punkty przerwania na powierzchni projektowej.  
  
-   QuickWatch.  
  
-   Ustaw następną instrukcję.  
  
-   Uruchom do kursora.  
  
-   Edytuj i Kontynuuj.  
  
-   Debugowanie just in time.  
  
-   Debugowanie w trybie mieszanym.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Wywoływanie debugera programu Visual Studio dla programu Windows Workflow Foundation (starsza wersja)](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [Wyłączanie debugera programu Visual Studio dla programu Windows Workflow Foundation (starsza wersja)](../workflow-designer/disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [Instrukcje: Debugowanie przepływów pracy opartych na programie ASP.NET (starsza wersja)](../workflow-designer/how-to-debug-aspnet-based-workflows-legacy.md)  
  
 [Instrukcje: Ustawianie punktów przerwania w przepływach pracy (starsza wersja)](../workflow-designer/how-to-set-breakpoints-in-workflows-legacy.md)  
  
 [Debugowanie przepływów pracy ze zdalnego komputera (starsza wersja)](../workflow-designer/debugging-workflows-from-a-remote-computer-legacy.md)  
  
 [Opcje debugowania wykonywania krokowego (starsza wersja)](../workflow-designer/debug-stepping-options-legacy.md)  
  
 [Instrukcje: Opcja zmiany debugowania krokowego (starsza wersja)](../workflow-designer/how-to-change-the-debug-stepping-option-legacy.md)