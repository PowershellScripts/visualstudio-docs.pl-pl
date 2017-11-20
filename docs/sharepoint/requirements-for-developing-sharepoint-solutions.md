---
title: "Wymagania związane z opracowywaniem rozwiązań SharePoint | Dokumentacja firmy Microsoft"
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
- SharePoint development in Visual Studio, prerequisites
- SharePoint development in Visual Studio, requirements
ms.assetid: ae8ff69d-4540-4380-ab0b-845f7108e89c
caps.latest.revision: "40"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a29eee363f3ad886d9ea6a13ee43475fba2e9448
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="requirements-for-developing-sharepoint-solutions"></a>Wymagania związane z opracowywaniem rozwiązań SharePoint
  W systemie należy zainstalować następujące wymagania wstępne, przed użyciem narzędzia deweloperskie rozwiązania programu SharePoint, uwzględnione w programie Visual Studio:  
  
-   [!INCLUDE[vsPro](../sharepoint/includes/vspro-md.md)]lub wersji programu Visual Studio cyklu życia zarządzania aplikacji (ALM).  
  
    -   Albo [!INCLUDE[csprcs](../sharepoint/includes/csprcs-md.md)] lub [!INCLUDE[vbprvb](../sharepoint/includes/vbprvb-md.md)] funkcji i/lub podczas instalowania [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].  
  
-   [!INCLUDE[moss_14_long](../sharepoint/includes/moss-14-long-md.md)]zainstalowane w 64-bitowej [!INCLUDE[winsvr08](../sharepoint/includes/winsvr08-md.md)] lub 64-bitowych [!INCLUDE[winsvr08](../sharepoint/includes/winsvr08-md.md)] R2.  
  
     lub  
  
-   [!INCLUDE[wss_14_long](../sharepoint/includes/wss-14-long-md.md)]zainstalowane w 64-bitowej [!INCLUDE[winsvr08](../sharepoint/includes/winsvr08-md.md)] lub 64-bitowych [!INCLUDE[winsvr08](../sharepoint/includes/winsvr08-md.md)] R2.  
  
> [!NOTE]  
>  Tylko systemy operacyjne serwera jest oficjalnie obsługiwana przez program SharePoint, systemami operacyjnymi klienta są dozwolone: [!INCLUDE[win7](../sharepoint/includes/win7-md.md)] i [!INCLUDE[windowsver](../sharepoint/includes/windowsver-md.md)] z dodatkiem SP1. Aby uzyskać więcej informacji, zobacz [Przewodnik instalacji programu SharePoint Server 2010 Developer stacji roboczej](http://go.microsoft.com/fwlink/?LinkID=164557).  
  
 Typy projektów modelu łączności danych (BDC) biznesowe wymagają, aby [!INCLUDE[moss_14_long](../sharepoint/includes/moss-14-long-md.md)] można zainstalować w systemie.  
  
 Umożliwiające tworzenie rozwiązań programu SharePoint w Visual Studio, programu SharePoint należy zainstalować na tym samym komputerze co program Visual Studio. Ponadto narzędzia SharePoint developer tools obsługują tylko konfiguracji autonomicznej SharePoint; nie obsługują konfiguracji farmy (zdalnego).  
  
> [!NOTE]  
>  Projekty programu SharePoint w Visual Studio obsługują tylko [!INCLUDE[net_v35_long](../sharepoint/includes/net-v35-long-md.md)]. W przypadku wybrania [!INCLUDE[net_v40_long](../sharepoint/includes/net-v40-long-md.md)] dla nowego projektu programu SharePoint, będzie nadal obowiązywać [!INCLUDE[net_v35_long](../sharepoint/includes/net-v35-long-md.md)].  
  
 Aby uzyskać więcej informacji o sposobie instalowania [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], zobacz [program Visual Studio](../install/install-visual-studio.md).  
  
## <a name="vista-and-windows-7-user-account-control-uac"></a>Kontrola konta użytkownika (UAC) w systemach Vista i Windows 7  
 [!INCLUDE[windowsver](../sharepoint/includes/windowsver-md.md)]i [!INCLUDE[win7](../sharepoint/includes/win7-md.md)] dołączyć do nich to funkcja zabezpieczeń, która jest znany jako kontroli konta użytkownika (UAC). Umożliwiające tworzenie rozwiązań programu SharePoint w [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] na [!INCLUDE[windowsver](../sharepoint/includes/windowsver-md.md)] i [!INCLUDE[win7](../sharepoint/includes/win7-md.md)] systemów kontroli konta użytkownika, użytkownik musi uruchomić [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] administrator systemu. Na pulpicie otwórz menu skrótów [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], a następnie wybierz pozycję **Uruchom jako administrator**.  
  
 Aby skonfigurować skrót zawsze Uruchom jako administrator, otwórz menu skrótów, wybierz pozycję **właściwości**, wybierz **zaawansowane** przycisk, a następnie wybierz **Uruchom jako administrator**  pole wyboru.  
  
 Aby uzyskać więcej informacji, zobacz [opis i konfigurowanie Kontrola konta użytkownika w systemie Windows Vista](http://go.microsoft.com/fwlink/?LinkID=156476). i [Kontrola konta użytkownika systemu Windows 7](http://go.microsoft.com/fwlink/?LinkId=177523).  
  
## <a name="sharepoint-permissions-considerations"></a>Uwagi dotyczące uprawnień programu SharePoint  
 Umożliwiające tworzenie rozwiązań programu SharePoint, musi mieć wystarczające uprawnienia do uruchamiania i debugowanie rozwiązań SharePoint. Zanim można przetestować rozwiązania programu SharePoint, wykonaj następujące kroki, aby upewnić się, że masz wystarczające uprawnienia:  
  
1.  Dodaj konto użytkownika jako administratora w systemie.  
  
2.  Dodaj konto użytkownika jako administratora farmy programu SharePoint server.  
  
    1.  W witrynie Administracja centralna programu SharePoint, wybierz **zarządzania do grupy administratorów farmy** łącza.  
  
    2.  Na **administratorzy farmy** wybierz pozycję **nowy** przycisku.  
  
3.  Dodaj konto użytkownika w grupie WSS_ADMIN_WPG uprawnienia.  
  
## <a name="see-also"></a>Zobacz też  
 [Wprowadzenie &#40; Projektowanie SharePoint w Visual Studio &#41;](../sharepoint/getting-started-sharepoint-development-in-visual-studio.md)  
  
  