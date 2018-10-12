---
title: 'Porady: generowanie szablonów z szablonów przy użyciu sekwencji unikowych | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- text templates, generating templates from templates
ms.assetid: 4126156a-7cea-48b8-925e-7790806cfe6c
caps.latest.revision: 37
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: fd3a54c69b33e503908217b9d0d83c6f61c6380a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49249421"
---
# <a name="how-to-generate-templates-from-templates-by-using-escape-sequences"></a>Porady: generowanie szablonów z szablonów przy użyciu sekwencji unikowych
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Można utworzyć szablon tekstowy, który tworzy inny szablon tekstowy jako dane wyjściowe wygenerowanego tekstu. Aby to zrobić, należy użyć sekwencje ucieczki aby odróżnić tagi szablonu tekstu. Jeśli nie korzystanie z sekwencji ucieczki, szablon wygenerowany tekst będzie mieć znaczenie wstępnie zdefiniowane. Aby uzyskać więcej informacji na temat przy użyciu sekwencji unikowych w szablonach tekstowych, zobacz [przy użyciu sekwencji unikowych w szablonach tekstowych](../modeling/using-escape-sequences-in-text-templates.md).  
  
### <a name="to-generate-a-text-template-from-within-a-text-template"></a>Aby wygenerować z szablonu tekstu w szablonie tekstu  
  
-   Użyj ukośnik odwrotny (\\) jako znak ucieczki do produkcji niezbędne znaczniki w szablonie tekstu dla dyrektywy, instrukcje, wyrażenia i funkcji w pliku szablonu tekstu oddzielne klasy.  
  
    ```  
    \<#@ directive \#>  
    \<# statement \#>  
    \<#= expression \#>  
    \<#+ classfeature \#>  
    ```  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie użyto znaki ucieczki, aby utworzyć szablon tekstowy z szablonu tekstu. `output` Dyrektywa określa docelowy typ pliku z typem pliku szablonu tekstu (.tt).  
  
```csharp  
\<#@ output extension=".tt" \#>  
\<#@ assembly name="System.Xml.dll" \#>  
\<#@ import namespace="System.Xml" \#>  
\<#  
XmlDocument xDoc = new XmlDocument();  
//System.Diagnostics.Debugger.Break();  
    xDoc.Load(@"E:\CSharp\Overview.xml");  
    XmlAttributeCollection attributes = xDoc.Attributes;  
    if (attributes != null)  
    {  
       foreach (XmlAttribute attr in attributes)  
       {\#>  
           \<#= attr.Name \#>  
       \<#}  
     }  
\#>  
```  
  
 Wygenerowany tekst wyjściowy jest szablonu tekstu.  
  
```  
<#@ output extension=".tt" #>  
<#@ assembly name="System.Xml.dll" #>  
<#@ import namespace="System.Xml" #>  
<#  
XmlDocument xDoc = new XmlDocument();  
//System.Diagnostics.Debugger.Break();  
    xDoc.Load(@"E:\CSharp\Overview.xml");  
    XmlAttributeCollection attributes = xDoc.Attributes;  
    if (attributes != null)  
    {  
       foreach (XmlAttribute attr in attributes)  
       {#>  
           <#= attr.Name #>  
       <#}  
     }  
#>  
```



