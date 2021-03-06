---
title: Tworzenie pakietu VSPackage kontroli źródła | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], creating source control packages
- source control packages
ms.assetid: cca0a9ed-48ff-409f-8036-ed8db0f7533e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0d9513410aa3bb4773629846abbd70159ec6aa77
ms.sourcegitcommit: 1c2ed640512ba613b3bbbc9ce348e28be6ca3e45
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/03/2018
ms.locfileid: "39499741"
---
# <a name="create-a-source-control-vspackage"></a>Tworzenie pakietu VSPackage kontroli źródła
Ta dokumentacja zawiera linki do omówienia architektury pakietu kontroli źródła, zintegrowana z usługą [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], interfejs API, który jest definiowany przez interfejsy, które mają być wdrożone i usług, które mają być używane, a przykład ilustrujący proste źródła Pakiet implementację formantu.  
  
 Za pomocą pakietu VSPackage z kontroli źródła, można utworzyć ścieżkę głęboka Integracja kontroli źródła zintegrować z usługą [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Umożliwia ona pakiet do obejścia kontroli źródła domyślnego interfejsu użytkownika pracujących [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], odpowiadanie na żądania kontroli źródła z projektu systemu i interakcji z [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] składniki, takie jak **Eksploratora rozwiązań**. [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Upoważnia [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] w ramach której partnerzy z mechanizmem do utworzenia pakietu VSPackage, który można zintegrować z [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] przy użyciu modelu usługi.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Wprowadzenie](../../extensibility/internals/getting-started-with-source-control-vspackages.md)  
 W tym artykule omówiono pakiet kontroli źródła, który jest bardziej zaawansowanych alternatywą do kontroli źródła wtyczek do implementowania funkcji kontroli źródła w [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].  
  
 [Architektura](../../extensibility/internals/source-control-vspackage-architecture.md)  
 Przedstawia informacje o diagramie i wyjaśniono składniki pakietu kontroli źródła.  
  
 [Funkcje](../../extensibility/internals/source-control-vspackage-features.md)  
 W tym artykule opisano różne funkcje pakietu kontroli źródła.  
  
 [Elementy projektu](../../extensibility/internals/source-control-vspackage-design-elements.md)  
 W tym artykule opisano Struktura pakietu VSPackage, który pakiet kontrolki źródła musi implementować do zaawansowanej integracji.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Tworzenie wtyczki kontroli źródła](../../extensibility/internals/creating-a-source-control-plug-in.md)  
 W tym artykule omówiono sposób tworzenia wtyczki kontroli źródła dostarczającego funkcji kontroli źródła w [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] interfejsu użytkownika kontroli źródła (UI).  
  
 [Kontrola źródła](../../extensibility/internals/source-control.md)  
 W tym artykule omówiono opcje implementowania kontroli źródła jako zintegrowaną funkcją [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].
