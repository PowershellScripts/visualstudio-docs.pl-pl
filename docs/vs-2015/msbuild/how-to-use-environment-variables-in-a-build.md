---
title: 'Porady: Użycie zmiennych środowiskowych w kompilacji | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- environment variables, referencing
- projects [.NET Framework], environment variables
- MSBuild, environment variables
ms.assetid: 7f9e4469-8865-4b59-aab3-3ff26bd36e77
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7a03b706957d6308dce90fb9f0dd2284338e7609
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49294617"
---
# <a name="how-to-use-environment-variables-in-a-build"></a>Porady: użycie zmiennych środowiskowych w kompilacji
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Podczas kompilowania projektów często jest to konieczne, można ustawić opcji kompilacji, korzystając z informacji, który nie znajduje się w pliku projektu lub plików, wchodzące w skład projektu. Te informacje są zwykle przechowywane w zmiennych środowiskowych.  
  
## <a name="referencing-environment-variables"></a>Odwoływanie się do zmiennych środowiskowych  
 Wszystkie zmienne środowiskowe są dostępne dla [!INCLUDE[vstecmsbuildengine](../includes/vstecmsbuildengine-md.md)] ([!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]) pliku projektu jako właściwości.  
  
> [!NOTE]
>  Jeśli plik projektu zawiera jawna definicja właściwości, która ma taką samą nazwę jak zmienna środowiskowa, właściwość w pliku projektu zastępuje wartość zmiennej środowiskowej.  
  
#### <a name="to-use-an-environment-variable-in-an-msbuild-project"></a>Aby użyć zmiennej środowiskowej w projekcie programu MSBuild  
  
-   Odwoływać się do zmiennej środowiskowej w taki sam sposób, jak Zmienna zadeklarowana w pliku projektu. Na przykład poniższy kod odwołuje się do zmiennej środowiskowej BIN_PATH:  
  
     `<FinalOutput>$(BIN_PATH)\MyAssembly.dll</FinalOutput>`  
  
 Możesz użyć `Condition` atrybutu, aby podać wartość domyślną dla właściwości, jeśli nie ustawiono zmiennej środowiskowej.  
  
#### <a name="to-provide-a-default-value-for-a-property"></a>Aby podać wartość domyślną dla właściwości  
  
-   Użyj `Condition` atrybutu dla właściwości, aby ustawić wartość tylko wtedy, gdy właściwość nie ma wartości. Na przykład, poniższy kod ustawia `ToolsPath` c:\tools tylko wtedy, gdy właściwość `ToolsPath` nie ustawiono zmiennej środowiskowej:  
  
     `<ToolsPath Condition="'$(TOOLSPATH)' == ''">c:\tools</ToolsPath>`  
  
    > [!NOTE]
    >  Nazwy właściwości nie jest rozróżniana wielkość liter więc zarówno `$(ToolsPath)` i `$(TOOLSPATH)` odwoływać się do tej samej zmiennej właściwości lub środowiska.  
  
## <a name="example"></a>Przykład  
 Następujący plik projektu używa zmiennych środowiskowych w celu określenia lokalizacji katalogów.  
  
```  
<Project DefaultTargets="FakeBuild">  
    <PropertyGroup>  
        <FinalOutput>$(BIN_PATH)\myassembly.dll</FinalOutput>  
        <ToolsPath Condition=" '$(ToolsPath)' == '' ">  
            C:\Tools  
        </ToolsPath>  
    </PropertyGroup>  
    <Target Name="FakeBuild">  
        <Message Text="Building $(FinalOutput) using the tools at $(ToolsPath)..."/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  

[MSBuild](msbuild.md)

[Właściwości programu MSBuild](../msbuild/msbuild-properties1.md)

[Instrukcje: Kompilacja tych samych plików źródłowych przy użyciu różnych opcji](../msbuild/how-to-build-the-same-source-files-with-different-options.md)


