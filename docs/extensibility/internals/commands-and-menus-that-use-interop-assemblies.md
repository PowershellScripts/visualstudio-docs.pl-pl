---
title: Polecenia i menu, które używają zestawów międzyoperacyjnych | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- menus, using interop assemblies
- interop assemblies, using in commands and menus
- commands, handling using interop assemblies
- command handling with interop assemblies
ms.assetid: 8f4af525-39e5-4e69-92c8-d3efabe80bb2
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 2212d9eb38487bf824fd8df3c497d9f256379c10
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49907810"
---
# <a name="commands-and-menus-that-use-interop-assemblies"></a>Polecenia i menu, które używają zestawów międzyoperacyjnych
Pakietu VSPackage, który implementuje poleceń menu i paska narzędzi przy użyciu zestawów międzyoperacyjnych musi:  
  
- Poinformuj [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] zintegrowanego środowiska programistycznego (IDE) dotyczące poleceń obsługuje i tego, czy są obecnie włączone.  
  
- Zgodne z regułami (Umowa) do obsługi poleceń.  
  
- Jawne Implementowanie obsługi poleceń przy użyciu <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> lub <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> interfejsu.  
  
  W poniższej sekcji opisano sposób wykonywania tych zadań.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Określenia stanu polecenia przy użyciu zestawów międzyoperacyjnych](../../extensibility/internals/determining-command-status-by-using-interop-assemblies.md)  
 W tym artykule opisano, jak pakietu VSPackage powiadamia IDE dotyczących poleceń, które obsługuje i tego, czy są obecnie włączone.  
  
 [Kontrakty poleceń w zestawach międzyoperacyjnych](../../extensibility/internals/command-contracts-in-interop-assemblies.md)  
 Zawiera definicję kontraktu podstawowe polecenia używane przez wszystkich pakietów VSPackage wykonania polecenia przy użyciu zestawów międzyoperacyjnych.
  
 [Implementacja poleceń](../../extensibility/internals/command-implementation.md)  
 Omówienie Implementowanie polecenia pakietu VSPackage.  
  
 [Zarejestruj procedury obsługi polecenia zestawu międzyoperacyjnego](../../extensibility/internals/registering-interop-assembly-command-handlers.md)  
 W tym artykule opisano wpisy rejestru wymagane do powiadamiania środowiska IDE, że pakietu VSPackage udostępnia procedurę obsługi poleceń.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Dostępność poleceń](../../extensibility/internals/command-availability.md)  
 W tym artykule opisano kryteria, które są używane przez środowisko IDE do określenia polecenia pakietu VSPackage, które są dostępne i jak obiekt je obsługuje.  
  
 [Jak dodać elementy interfejsu użytkownika w pakietach VSPackage](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)  
 Zawiera szczegółowe informacje o sposobie tworzenia interfejsu użytkownika, który używa [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] polecenia pomocy technicznej.  
  
 [Routing poleceń w pakietach VSPackage](../../extensibility/internals/command-routing-in-vspackages.md)  
 Przegląd procesu umożliwiającego odnoszą się obiektu z żądaniem odpowiednie polecenie.