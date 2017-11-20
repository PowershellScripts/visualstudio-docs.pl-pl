---
title: "Przy użyciu i udostępnia usługi | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- examples [Visual Studio SDK], services
- Visual Studio, services
- services
ms.assetid: c0b415ba-b825-4da0-9faf-8a60a663e302
caps.latest.revision: "41"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e28b66dea8440c969926abd3892739f4e041b064
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="using-and-providing-services"></a>Przy użyciu i świadczenia usług
Usługa jest Umowa między dwoma VSPackages. Jeden pakiet VSPackage oferuje określony zbiór interfejsów dla innego pakiet VSPackage korzystać. Na przykład [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] oferuje <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> do dowolnego pakiet VSPackage go obsłużyć obciążenia. Ta usługa udostępnia <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog> interfejs, który może służyć do zapisu w dzienniku aktywności. Aby uzyskać więcej informacji, zobacz [porady: Korzystanie z dziennika aktywności](../extensibility/how-to-use-the-activity-log.md).  
  
 VSPackages mogą oferować własnych przy użyciu usług <xref:Microsoft.VisualStudio.Shell.Interop.IProfferService> interfejsu.  
  
 Program Visual Studio oferuje ważne usługi, takie jak następujące:  
  
|Usługa IDE|Opis|  
|-----------------|-----------------|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsShell>|Zapewnia dostęp do środowiska IDE usług postępowania z podstawowymi funkcjami, VSPackages i rejestru.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell>|Udostępnia podstawowe okien i funkcji związanych z interfejsu użytkownika w środowisku IDE, takie jak możliwość tworzenia okna dokumentów i narzędzia.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.SVsSolution>|Udostępnia podstawowe funkcje związane z rozwiązania, takie jak możliwość wyliczyć projektów, tworzenie nowych projektów i monitorowanie zmian projektu.|  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Usługa Essentials](../extensibility/internals/service-essentials.md)  
 Przedstawia informacje o ważne elementy usługi Visual Studio.  
  
 [Porady: uzyskiwanie usługi](../extensibility/how-to-get-a-service.md)  
 W tym artykule omówiono sposób żądania (korzystać) usługi.  
  
 [Porady: udostępnianie usługi](../extensibility/how-to-provide-a-service.md)  
 W tym artykule omówiono sposób do świadczenia usług.  
  
 [Porady: Podaj usługa asynchronicznego programu Visual Studio](../extensibility/how-to-provide-an-asynchronous-visual-studio-service.md)  
 Omówiono sposób obsługi asynchronicznego.  
  
 [Porady: Rozwiązywanie problemów z usługami](../extensibility/how-to-troubleshoot-services.md)  
 W tym artykule omówiono typowe problemy i przedstawia ich rozwiązania.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Visual Studio SDK](../extensibility/visual-studio-sdk.md)