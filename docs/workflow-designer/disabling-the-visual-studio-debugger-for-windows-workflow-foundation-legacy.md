---
title: "Wyłączenie debugera programu Visual Studio dla programu Windows Workflow Foundation (starsze) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- workflows, disabling debugger
- debugging workflows, disabling debugger
- workflow debugger, disabling
ms.assetid: 9da96d0e-f941-4fa9-a1a5-6bab50adfec9
caps.latest.revision: "6"
author: ErikRe
ms.author: erikre
manager: erikre
ms.openlocfilehash: 835ca509c86a9be27486ee257839c4e161221e4e
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy"></a>Wyłączenie debugera programu Visual Studio dla programu Windows Workflow Foundation (starsze)
W tym temacie opisano sposób wyłączania [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] debugera przy użyciu pliku konfiguracji podczas kompilowania [!INCLUDE[wf](../workflow-designer/includes/wf_md.md)] aplikacji w starszych [!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)]. Użyj starszego [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] konieczność docelowy: [!INCLUDE[netfx35_long](../workflow-designer/includes/netfx35_long_md.md)] lub [!INCLUDE[vstecwinfx](../workflow-designer/includes/vstecwinfx_md.md)].  
  
 Domyślnie [!INCLUDE[vs_current_long](../misc/includes/vs_current_long_md.md)] debugera dla [!INCLUDE[wf](../workflow-designer/includes/wf_md.md)] jest włączona dla procesu hosta. Aby wyłączyć debugowanie przepływu pracy, musisz jawnie wyłączyć ją, dodając wpis "DisableWorkflowDebugging"  **\<przełączniki >** element  **\<system.diagnostics >**sekcji pliku konfiguracji hosta.  
  
 Poniższy przykład przedstawia sposób modyfikowania hosta pliku konfiguracji, aby wyłączyć debugowanie przepływu pracy.  
  
```  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
   <system.diagnostics>  
      <switches>  
         <add name="DisableWorkflowDebugging" value="true"/>  
      </switches>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Wywoływanie debugera programu Visual Studio dla programu Windows Workflow Foundation (starsze)](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)   
 [Debugowanie przepływów pracy starsza wersja](../workflow-designer/debugging-legacy-workflows.md)