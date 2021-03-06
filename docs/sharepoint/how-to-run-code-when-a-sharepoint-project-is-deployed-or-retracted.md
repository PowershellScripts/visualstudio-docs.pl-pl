---
title: 'Porady: uruchamianie kodu gdy projekt SharePoint jest wdrożony lub wycofany | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, extending deployment
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: da1b6dd4ff71bcc78043ea88c8f833b9c0f32a38
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49832449"
---
# <a name="how-to-run-code-when-a-sharepoint-project-is-deployed-or-retracted"></a>Porady: uruchamianie kodu, podczas projektu programu SharePoint jest wdrożony lub wycofany
  Jeśli chcesz wykonać dodatkowe zadania, podczas projektu programu SharePoint jest wdrożony lub wycofany, może obsługiwać zdarzenia, które są wywoływane przez program Visual Studio. Aby uzyskać więcej informacji, zobacz [pakowaniem i wdrażaniem SharePoint rozszerzyć](../sharepoint/extending-sharepoint-packaging-and-deployment.md).  
  
### <a name="to-run-code-when-a-sharepoint-project-is-deployed-or-retracted"></a>Do uruchomienia kodu, podczas projektu programu SharePoint jest wdrożony lub wycofany  
  
1. Tworzenie rozszerzenia elementu projektu, rozszerzenia projektu lub definicji typu elementu projektu. Więcej informacji znajduje się w następujących tematach:  
  
   -   [Porady: Tworzenie rozszerzenia elementu projektu SharePoint](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)  
  
   -   [Porady: Tworzenie rozszerzenia projektu SharePoint](../sharepoint/how-to-create-a-sharepoint-project-extension.md)  
  
   -   [Porady: Definiowanie typu elementu projektu SharePoint](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)  
  
2. W rozszerzeniu usługi dostęp <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService> obiektu. Aby uzyskać więcej informacji, zobacz [porady: pobieranie usługi projektu SharePoint](../sharepoint/how-to-retrieve-the-sharepoint-project-service.md).  
  
3. Obsługa <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentStarted> i <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentCompleted> zdarzenia z usługi projektu.  
  
4. W przypadku programów obsługi, użyj <xref:Microsoft.VisualStudio.SharePoint.DeploymentEventArgs> parametru, aby uzyskać informacje na temat bieżącej sesji wdrożenia. Na przykład możesz określić, której projekt jest w bieżącej sesji, wdrożenia i tego, czy jest wdrożony lub wycofany.  
  
   Poniższy przykład kodu demonstruje sposób obsługi <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentStarted> i <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentCompleted> zdarzenia w rozszerzeniu projektu. To rozszerzenie zapisuje komunikat dodatkowe do **dane wyjściowe** okna, gdy wdrożenie rozpoczyna się i zakończy się dla projektu programu SharePoint.  
  
   [!code-csharp[SPExtensibility.ProjectSystemExtension.General#12](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/handleprojectdeploymentevents.cs#12)]
   [!code-vb[SPExtensibility.ProjectSystemExtension.General#12](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/handleprojectdeploymentevents.vb#12)]  
  
## <a name="compile-the-code"></a>Skompilować kod  
 Ten przykład wymaga odwołania do następujących zestawów:  
  
-   Microsoft.VisualStudio.SharePoint  
  
-   System.ComponentModel.Composition  
  
## <a name="deploy-the-extension"></a>Wdrażanie rozszerzenia  
 Aby wdrożyć rozszerzenie, należy utworzyć [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] rozszerzenie (VSIX), pakiet dla zestawu i innych plików, które chcesz dystrybuować z rozszerzeniem. Aby uzyskać więcej informacji, zobacz [wdrażanie rozszerzeń dla narzędzi SharePoint w programie Visual Studio](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Zobacz także
 [Rozszerzanie pakowania i wdrażania SharePoint](../sharepoint/extending-sharepoint-packaging-and-deployment.md)   
 [Porady: uruchamianie kodu, gdy są wykonywane kroki związane z wdrażaniem](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md)  
  
