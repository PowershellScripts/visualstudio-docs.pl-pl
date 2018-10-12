---
title: Element metadanych w przetwarzaniu wsadowym obiektów docelowych | Dokumentacja firmy Microsoft
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
- batching [MSBuild]
- MSBuild, target batching
- target batching [MSBuild]
ms.assetid: f3cc4186-6a4c-4161-bbe5-1ec638b4925b
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 011bb9b738aa135fd14c4dbddfb26f9cea2f7bd1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49232691"
---
# <a name="item-metadata-in-target-batching"></a>Metadane elementu w przetwarzaniu wsadowym obiektów docelowych
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] zdolność przeprowadzania analizy zależności wejść i wyjść docelowej kompilacji. Jeśli okaże się, że dane wejściowe lub wyjściowe, obiektu docelowego są aktualne, element docelowy zostanie pominięta, a kompilacja będzie kontynuować. `Target` Użyj elementów `Inputs` i `Outputs` atrybutów, aby określić elementy, aby sprawdzić podczas analizy zależności.  
  
 Jeśli obiekt docelowy zawiera zadania, które używa elementy w partii jako danych wejściowych lub wyjściowych, `Target` elementu docelowego należy używać, przetwarzanie wsadowe w jego `Inputs` lub `Outputs` atrybutów, aby umożliwić [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] do pominięcia instancji elementów, które są już aktualne.  
  
## <a name="batching-targets"></a>Przetwarzanie wsadowe obiektów docelowych  
 Poniższy przykład zawiera listę elementów o nazwie `Res` który jest podzielony na dwie partie na podstawie `Culture` metadanych elementu. Każda z tych partii jest przekazywana do `AL` zadania, które tworzy zestaw danych wyjściowych dla każdej partii. Za pomocą adapterów przetwarzania wsadowego na `Outputs` atrybutu `Target` elementu [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] można określić, czy jest każdej partii poszczególnych aktualne przed uruchomieniem element docelowy. Bez użycia przetwarzaniu wsadowym obiektów docelowych, zarówno partie elementów zostałoby uruchomione przez zadanie podrzędne, za każdym razem, gdy element docelowy został wykonany.  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <Res Include="Strings.fr.resources">  
            <Culture>fr</Culture>  
        </Res>  
        <Res Include="Strings.jp.resources">  
            <Culture>jp</Culture>  
        </Res>  
        <Res Include="Menus.fr.resources">  
            <Culture>fr</Culture>  
        </Res>  
        <Res Include="Dialogs.fr.resources">  
            <Culture>fr</Culture>  
        </Res>  
        <Res Include="Dialogs.jp.resources">  
            <Culture>jp</Culture>  
        </Res>  
        <Res Include="Menus.jp.resources">  
            <Culture>jp</Culture>  
        </Res>  
    </ItemGroup>  
  
    <Target Name="Build"  
        Inputs="@(Res)"  
        Outputs="%(Culture)\MyApp.resources.dll">  
  
        <AL Resources="@(Res)"  
            TargetType="library"  
            OutputAssembly="%(Culture)\MyApp.resources.dll"  
  
    </Target>  
  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: kompilacja przyrostowa](../msbuild/how-to-build-incrementally.md)   
 [Przetwarzanie wsadowe](../msbuild/msbuild-batching.md)   
 [TARGET — Element (MSBuild)](../msbuild/target-element-msbuild.md)   
 [Metadane elementu w przetwarzaniu wsadowym zadań](../msbuild/item-metadata-in-task-batching.md)



