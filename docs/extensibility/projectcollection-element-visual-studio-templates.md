---
title: "Projectcollection — Element (szablony Visual Studio) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/vstemplate/2005#ProjectCollection
helpviewer_keywords:
- <ProjectCollection> element [Visual Studio Templates]
- ProjectCollection element [Visual Studio Templates]
ms.assetid: deb27180-2035-49ed-b835-c47bb3cd2f8f
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d043d9963ad9f2bf9bd06b7a8cc543ffaee50e19
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="projectcollection-element-visual-studio-templates"></a>ProjectCollection — Element (szablony Visual Studio)
Określa organizację i zawartość szablonów wieloprojektowych.  
  
 \<VSTemplate >  
 \<TemplateContent >  
 \<Projectcollection — >  
  
## <a name="syntax"></a>Składnia  
  
```  
<ProjectCollection>  
    <ProjectTemplateLink> ... </ProjectTemplateLink>  
    <SolutionFolder> ... </SolutionFolder>  
</ProjectCollection>  
```  
  
## <a name="attributes-and-elements"></a>Atrybuty i elementy  
 W poniższych sekcjach opisano atrybut, elementy podrzędne i elementy nadrzędne.  
  
### <a name="attributes"></a>Atrybuty  
 Brak.  
  
### <a name="child-elements"></a>Elementy podrzędne  
  
|Element|Opis|  
|-------------|-----------------|  
|[Projecttemplatelink —](../extensibility/projecttemplatelink-element-visual-studio-templates.md)|Element opcjonalny.<br /><br /> Określa projekt, w szablonie wielu projektów.|  
|[SolutionFolder](../extensibility/solutionfolder-element-visual-studio-templates.md)|Element opcjonalny.<br /><br /> Grupowanie projektów w szablonach wieloprojektowych.|  
  
### <a name="parent-elements"></a>Elementy nadrzędne  
  
|Element|Opis|  
|-------------|-----------------|  
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Element wymagany.<br /><br /> Określa zawartość szablonu.|  
  
## <a name="remarks"></a>Uwagi  
 Szablony wieloprojektowe działają jak kontenery dla dwóch lub więcej projektów. `ProjectCollection` Element służy do określania projektów, które zawierają w szablonie. Aby uzyskać więcej informacji dotyczących szablonów wielu projektów, zobacz [porady: Tworzenie szablonów wielu projektów](../ide/how-to-create-multi-project-templates.md).  
  
## <a name="example"></a>Przykład  
 W tym przykładzie pokazano prosty główny plik .vstemplate szablonu wieloprojektowego. W tym przykładzie szablon zawiera dwa projekty `My Windows Application` i `My Class Library`. `ProjectName` Atrybutu `ProjectTemplateLink` element ustawia nazwę [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] można przypisać tego projektu. Jeśli `ProjectName` atrybut nie istnieje, nazwa pliku .vstemplate jest używana jako nazwa projektu.  
  
```  
<VSTemplate Version="3.0.0" Type="ProjectGroup"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>Multi-Project Template Sample</Name>  
        <Description>An example of a multi-project template</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>VisualBasic</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectCollection>  
            <ProjectTemplateLink ProjectName="My Windows Application">  
                WindowsApp\MyTemplate.vstemplate  
            </ProjectTemplateLink>  
            <ProjectTemplateLink ProjectName="My Class Library">  
                ClassLib\MyTemplate.vstemplate  
            </ProjectTemplateLink>  
        </ProjectCollection>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do schematu szablonu Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Tworzenie szablony projektów i elementów](../ide/creating-project-and-item-templates.md)   
 [Porady: Tworzenie szablonów wielu projektów](../ide/how-to-create-multi-project-templates.md)