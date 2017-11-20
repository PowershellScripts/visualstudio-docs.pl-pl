---
title: "Porady: Tworzenie funkcji niestandardowej oraz zasady walidacji pakietu dla rozwiązań SharePoint | Dokumentacja firmy Microsoft"
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
helpviewer_keywords:
- SharePoint development in Visual Studio, extending deployment
- SharePoint development in Visual Studio, validation rules
ms.assetid: 17e818f8-0f3a-4a96-a6fc-1634ddb4825d
caps.latest.revision: "18"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 7a4b2c9bb828fb8c8b55829a4a6a295bb8324361
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions"></a>Porady: tworzenie funkcji niestandardowej oraz zasady walidacji pakietu dla Rozwiązań SharePoint
  Można utworzyć niestandardowe reguły walidacji można zweryfikować pakietu rozwiązania generowane przez program Visual Studio. Można wykonać pełnej weryfikacji w całej funkcji lub pakietu, wybierając **weryfikacji** z menu kontekstowego pakietu lub funkcji w **PackagingExplorer**. Częściowego sprawdzania poprawności jest wykonywane podczas dodawania nowych elementów projektu SharePonit lub funkcje do projektu, aby określić pakietu lub funkcji działałoby w prawidłowym stanie.  
  
### <a name="to-create-a-custom-package-validation-rule"></a>Aby utworzyć regułę sprawdzania poprawności pakietu niestandardowego  
  
1.  Tworzenie projektu biblioteki klas.  
  
2.  Dodaj odwołania do następujących zestawów:  
  
    -   Microsoft.VisualStudio.SharePoint  
  
    -   System.ComponentModel.Composition  
  
3.  Utwórz klasę, która implementuje jednej z następujących interfejsów:  
  
    -   Aby utworzyć reguły sprawdzania poprawności pakietu, należy zaimplementować <xref:Microsoft.VisualStudio.SharePoint.Validation.IPackageValidationRule> interfejsu.  
  
    -   Aby utworzyć regułę funkcji sprawdzania poprawności, zaimplementuj <xref:Microsoft.VisualStudio.SharePoint.Validation.IFeatureValidationRule> interfejsu.  
  
4.  Dodaj <xref:System.ComponentModel.Composition.ExportAttribute> do klasy. Ten atrybut umożliwia Visual Studio, aby odnaleźć i załadować reguły sprawdzania poprawności. Przekaż <xref:Microsoft.VisualStudio.SharePoint.Validation.IPackageValidationRule> lub <xref:Microsoft.VisualStudio.SharePoint.Validation.IFeatureValidationRule> typu konstruktora atrybutu.  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie pokazano, jak utworzyć niestandardowe reguły walidacji funkcji.  
  
 [!code-vb[SPExtensibility.FeatureValidation#1](../sharepoint/codesnippet/VisualBasic/featurevalidation/extension/customvalidationrule.vb#1)]
 [!code-csharp[SPExtensibility.FeatureValidation#1](../sharepoint/codesnippet/CSharp/featurevalidation/extension/customfeaturevalidationrule.cs#1)]  
  
## <a name="compiling-the-code"></a>Kompilowanie kodu  
 W tym przykładzie wymaga odwołania do następujących zestawów:  
  
-   Microsoft.VisualStudio.SharePoint.  
  
-   System.ComponentModel.Composition.  
  
## <a name="deploying-the-extension"></a>Wdrażanie rozszerzenia  
 Aby wdrożyć rozszerzenie, należy utworzyć [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] pakietu rozszerzenia (VSIX) dla zestawu i inne pliki, które chcesz dystrybuować z rozszerzeniem. Aby uzyskać więcej informacji, zobacz [wdrażanie rozszerzeń dla narzędzi SharePoint w Visual Studio](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Rozszerzanie pakowania i wdrażania SharePoint](../sharepoint/extending-sharepoint-packaging-and-deployment.md)  
  
  