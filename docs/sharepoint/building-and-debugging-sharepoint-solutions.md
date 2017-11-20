---
title: "Kompilowanie i debugowanie rozwiązań SharePoint | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, building and debugging
- SharePoint development in Visual Studio, debugging
ms.assetid: c9e7c9ab-4eb3-40cd-a9b9-6c2a896f70ae
caps.latest.revision: "14"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7582b0bcef8a97de14fb3b931745d6dcc21fa876
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="building-and-debugging-sharepoint-solutions"></a>Kompilowanie i debugowanie rozwiązań SharePoint
  Ogólnie rzecz biorąc, kompilowanie i debugowanie rozwiązań SharePoint jest taka sama jak kompilowanie i debugowanie innych typów projektów w [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. W tematach w tej sekcji opisano różnice, które istnieją.  
  
## <a name="project-output-for-sharepoint-solutions"></a>Dane wyjściowe projektu dla rozwiązań SharePoint  
 Tworzenie rozwiązań programu SharePoint tworzy zestawów i rozwiązania pakietu (wsp). W poniższej tabeli przedstawiono lokalizacje plików podczas kompilacji.  
  
|Tworzenie elementu|Folder wyjściowy|  
|----------------|-------------------|  
|Zestaw, bazy danych programu (PDB) i pliki WSP.|*ProjectName*\bin\debug lub *ProjectName*\bin\release|  
|Pliki elementu projektu SharePoint.|*ProjectName*\pkg\debug lub *ProjectName*\pkg\release|  
|Tworzenie plików pośrednich.|*ProjectName*\obj\debug lub *ProjectName*\obj\release|  
|Pakiet plików pośrednich.|*ProjectName*\pkgobj\debug lub *ProjectName*\pkgobj\release|  
  
## <a name="building-sharepoint-solutions"></a>Tworzenie rozwiązań programu SharePoint  
 Tworzenie rozwiązań programu SharePoint, na komputerze deweloperskim musi mieć poprawną wersję programu SharePoint server. W przeciwnym razie tworzenie rozwiązań programu SharePoint jest taka sama jak tworzenie innych typów projektów w [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Aby uzyskać więcej informacji, zobacz [porady: tworzenie rozwiązań programu SharePoint](../sharepoint/how-to-build-sharepoint-solutions.md).  
  
## <a name="debugging-and-testing-sharepoint-solutions"></a>Debugowanie i testowanie rozwiązań SharePoint  
 Przed debugowania, [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] kopiuje pakiet WSP na serwer programu SharePoint, aktywuje lokacji i funkcji należących do zakresu sieci Web i w niektórych przypadkach uruchamia projektu. W innych przypadkach może być konieczne ręczne Otwórz projekt. Aby uzyskać więcej informacji, zobacz [Rozwiązywanie problemów z rozwiązań SharePoint](../sharepoint/troubleshooting-sharepoint-solutions.md) i [debugowanie rozwiązań SharePoint](../sharepoint/debugging-sharepoint-solutions.md).  
  
## <a name="debugging-and-verifying-sharepoint-solutions-by-using-alm-features"></a>Debugowanie i sprawdzania poprawności rozwiązań programu SharePoint przy użyciu funkcji ALM  
 Visual Studio ALM funkcje takie jak testy jednostkowe i IntelliTrace włączyć więcej problemów znaleźć dokładnie w ramach rozwiązań programu SharePoint. Profilowanie umożliwia lokalizację i identyfikację problemów wydajności w ramach rozwiązań programu SharePoint. Aby uzyskać więcej informacji, zobacz [weryfikacji i debugowanie kodu aplikacji programu SharePoint](../sharepoint/verifying-and-debugging-sharepoint-code.md) i [profilowanie wydajności aplikacji SharePoint](../sharepoint/profiling-the-performance-of-sharepoint-applications.md).  
  
## <a name="security-during-the-build-process"></a>Zabezpieczeń podczas procesu kompilacji  
 Do pakietu lub wdrożenia rozwiązań SharePoint [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] musi mieć uprawnienie do kopiowania plików do serwera programu SharePoint. Należy uruchomić [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] jako procesów z podwyższonym poziomem uprawnień i użytkownika konto musi być administratorem kolekcji witryn na serwerze programu SharePoint. Ponadto należy określić, czy projekt jest rozwiązania typu piaskownica lub rozwiązaniu farmy. Aby uzyskać więcej informacji, zobacz [różnice między rozwiązaniami w trybie piaskownicy oraz rozwiązaniami farmy](../sharepoint/differences-between-sandboxed-and-farm-solutions.md).  
  
## <a name="using-the-clean-command"></a>Za pomocą polecenia Clean  
 Rozwiązania programu SharePoint jest zainstalowany na serwerze programu SharePoint do debugowania, **wyczyść** polecenie nie powoduje odinstalowania rozwiązania. Zamiast tego należy dezaktywować funkcji za pomocą konfiguracji programu SharePoint.  
  
## <a name="see-also"></a>Zobacz też  
 [Opracowywanie rozwiązań SharePoint](../sharepoint/developing-sharepoint-solutions.md)   
 [Przeglądanie połączeń SharePoint za pomocą Eksploratora serwera](../sharepoint/browsing-sharepoint-connections-using-server-explorer.md)   
 [Pakowanie i wdrażanie rozwiązań SharePoint](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
  
  