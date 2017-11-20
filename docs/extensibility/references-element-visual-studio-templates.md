---
title: "Odwołuje się Element (szablony Visual Studio) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/vstemplate/2005#References
helpviewer_keywords:
- <References> element [Visual Studio Templates]
- References element [Visual Studio Templates]
ms.assetid: 1969146d-46bf-422d-8d46-0e9493925003
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 436b5f745dc9b3b8c135ad111e6e708bbd391b4e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="references-element-visual-studio-templates"></a>Odwołania — element (szablony Visual Studio)
Grupy odwołania do zestawów, które do szablonu dodawany do projektów.  
  
 \<VSTemplate >  
 \<TemplateContent >  
 \<Odwołania >  
  
## <a name="syntax"></a>Składnia  
  
```  
<References>  
    <Reference>... </Reference>  
    <Reference>... </Reference>  
    ...  
</References>  
```  
  
## <a name="attributes-and-elements"></a>Atrybuty i elementy  
 W poniższych sekcjach opisano atrybut, elementy podrzędne i elementy nadrzędne.  
  
### <a name="attributes"></a>Atrybuty  
 Brak.  
  
### <a name="child-elements"></a>Elementy podrzędne  
  
|Element|Opis|  
|-------------|-----------------|  
|[Odwołanie](../extensibility/reference-element-visual-studio-templates.md)|Element wymagany.<br /><br /> Określa odwołanie do zestawu, aby dodać, gdy element zostanie dodany do projektu. Musi istnieć co najmniej jeden `Reference` elementów w `References` elementu.|  
  
### <a name="parent-elements"></a>Elementy nadrzędne  
  
|Element|Opis|  
|-------------|-----------------|  
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|Określa zawartość szablonu.|  
  
## <a name="remarks"></a>Uwagi  
 `References`jest elementem podrzędnym opcjonalne `TemplateContent`.  
  
 `Reference` i `References` elementów można używać tylko w plikach .vstemplate `Type` wartość atrybutu `Item`.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład przedstawia `TemplateContent` element szablonu elementu. Plik XML dodaje odwołania do zestawów System.dll i System.Data.dll.  
  
```  
<TemplateContent>  
    <References>  
        <Reference>  
            <Assembly>  
                System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089  
            </Assembly>  
        </Reference>  
        <Reference>  
            <Assembly>  
                System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089  
            </Assembly>  
        </Reference>  
    </References>  
    ...  
</TemplateContent>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do schematu szablonu Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Tworzenie szablony projektów i elementów](../ide/creating-project-and-item-templates.md)