---
title: Visual Studio Shell | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- shell, Visual Studio
- Visual Studio, shell
ms.assetid: cb124ef4-1a6b-4bfe-bfbf-295ef9c07f36
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 63b8420b3941114f8edd1e494c8469ae4b81ba79
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="visual-studio-shell"></a>Visual Studio Shell
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Powłoki jest podstawowym agenta integracji w [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Powłoka udostępnia funkcje niezbędne umożliwiające VSPackages do udostępniania usług wspólnej. Ponieważ architektury celem [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ma uprawnienia nabywa podstawowe funkcje w VSPackages, powłoka jest framework zapewnienia podstawowej funkcjonalności i obsługę techniczną, cross komunikacji między jego składnika VSPackages.  
  
## <a name="shell-responsibilities"></a>Obowiązki powłoki  
 Powłoka ma następujące obowiązki klucza:  
  
-   Obsługa (za pośrednictwem interfejsów COM) podstawowe elementy interfejsu użytkownika (UI). Obejmują one domyślnych menu i pasków narzędzi, ramki okna dokumentu lub okno podrzędne interfejsu wielu dokumentów (MDI) i ramki okna narzędzi i dokujące pomocy technicznej.  
  
-   Obsługa listę uruchomionych wszystkie aktualnie otwarte dokumenty w uruchomionej tabeli dokumentu (Normalizacją) w celu koordynowania trwałości dokumentów i gwarantuje, że nie można otworzyć tego dokumentu co w więcej niż jeden sposób lub w sposób niezgodny.  
  
-   Obsługa interfejsu routing poleceń i polecenia obsługi `IOleCommandTarget`.  
  
-   Ładowanie VSPackages w odpowiednim czasie. Opóźnienie ładowania pakiet VSPackage jest niezbędne do zwiększania wydajności powłoki.  
  
-   Zarządzanie niektórych udostępnionymi usług, takich jak <xref:Microsoft.VisualStudio.Shell.Interop.SVsShell>, która udostępnia funkcje podstawowe powłoki, i <xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell>, która dostarcza funkcje podstawowe okien.  
  
-   Zarządzanie plikami solution (.sln). Rozwiązania zawiera grupy projektów pokrewnych, podobnie jak plików obszaru roboczego (.dsw) w programie Visual C++ 6.0.  
  
-   Śledzenie zaznaczenia całej powłoki, kontekstu i waluty. Powłoka śledzi następujące elementy:  
  
    -   Bieżący projekt  
  
    -   Bieżący element projektu lub identyfikator bieżącego elementu<xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy>  
  
    -   Bieżące zaznaczenie dla **właściwości** okna lub`SelectionContainer`  
  
    -   Kontekst interfejsu użytkownika lub identyfikatory CmdUIGuids sterowania widoczności poleceń, menu i pasków narzędzi  
  
    -   Obecnie aktywnych elementów, takich jak aktywne okno dokumentu i menedżera cofania  
  
    -   Atrybuty kontekstu użytkownika, które dysków dynamiczna pomoc  
  
 Powłoka przekazuje także komunikacji między zainstalowane pakiety VSPackage i bieżącej usługi. Obsługuje podstawowe funkcje powłoki i udostępnia je wszystkie pakiety VSPackage zintegrowany [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Te podstawowe funkcje obejmują następujące elementy:  
  
-   **O** ekranu okna dialogowego pole i powitalny  
  
-   **Dodaj nowy i Dodaj istniejący element** okien dialogowych  
  
-   **Widok klasy** okna i **przeglądarki obiektów**  
  
-   **Odwołania** — okno dialogowe  
  
-   **Konspekt dokumentu** okna  
  
-   **Pomoc dynamiczna** okna  
  
-   **Znajdź** i **Zamień**  
  
-   **Otwórz projekt** i **Otwórz plik** okien dialogowych na **nowy** menu  
  
-   **Opcje** okno dialogowe na **narzędzia** menu  
  
-   **Właściwości** okna  
  
-   **Eksplorator rozwiązań**  
  
-   **Lista zadań** okna  
  
-   **Przybornika**  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy>   
 <xref:Microsoft.VisualStudio.Shell.Interop.SVsShell>   
 <xref:Microsoft.VisualStudio.Shell.Interop.SVsUIShell>   
 [VSPackages](../../extensibility/internals/vspackages.md)