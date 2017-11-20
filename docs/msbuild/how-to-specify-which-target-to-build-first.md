---
title: "Porady: Określanie obiektu docelowego do kompilacji najpierw | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- DefaultTargets attribute [MSBuild]
- MSBuild, specifying the defalut target
- MSBuild, DefaultTargets attribute
ms.assetid: a580ba5b-2919-42d2-ae38-1af991e0205a
caps.latest.revision: "17"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 22c307129e1c0295b041180f475c3d905cc43539
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-specify-which-target-to-build-first"></a>Porady: określanie pierwszego obiektu docelowego do kompilacji
Plik projektu może zawierać jeden lub więcej `Target` elementów, które określają jak projekt jest budowany. [!INCLUDE[vstecmsbuildengine](../msbuild/includes/vstecmsbuildengine_md.md)] ([!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]) Aparatu kompilacji pierwszy projektu go znajduje oraz wszelkie zależności, chyba że plik projektu zawiera `DefaultTargets` atrybutu `InitialTargets` atrybut lub element docelowy jest określona za pomocą wiersza polecenia **/ docelowy** przełącznika.  
  
## <a name="using-the-initialtargets-attribute"></a>Za pomocą atrybutu InitialTargets  
 `InitialTargets` Atrybutu `Project` element Określa docelowych, które zostanie uruchomione po pierwsze, nawet jeśli obiekty docelowe są określone w wierszu polecenia lub w `DefaultTargets` atrybutu.  
  
#### <a name="to-specify-one-initial-target"></a>Aby określić jeden cel początkowej  
  
-   Określ domyślny obiekt docelowy `InitialTargets` atrybutu `Project` elementu. Na przykład:  
  
     `<Project InitialTargets="Clean">`  
  
 Można określić więcej niż jeden cel początkowej w `InitialTargets` atrybut wyświetlania elementów docelowych w kolejności, a za pomocą średnika do rozdzielenia każdego obiektu docelowego. Obiekty docelowe, na liście będzie wykonywane sekwencyjnie.  
  
#### <a name="to-specify-more-than-one-initial-target"></a>Aby określić więcej niż jeden element docelowy początkowej  
  
-   Początkowe cele, oddzielone średnikami w listy `InitialTargets` atrybutu `Project` elementu. Na przykład, aby uruchomić `Clean` docelowego, a następnie `Compile` docelowych, wpisz:  
  
     `<Project InitialTargets="Clean;Compile">`  
  
## <a name="using-the-defaulttargets-attribute"></a>Przy użyciu defaulttargets — atrybut  
 `DefaultTargets` Atrybutu `Project` element określa, które docelowej lub miejsc docelowych są wbudowane, jeśli element docelowy nie jest jawnie określona w wierszu polecenia. Jeśli nie określono elementów docelowych w obu `InitialTargets` i `DefaultTargets` atrybuty i docelowy nie jest określona w wierszu polecenia [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] uruchamia cele określone w `InitialTargets` atrybutu następuje cele określone w `DefaultTargets` atrybut.  
  
#### <a name="to-specify-one-default-target"></a>Aby określić jeden domyślny obiekt docelowy  
  
-   Określ domyślny obiekt docelowy `DefaultTargets` atrybutu `Project` elementu. Na przykład:  
  
     `<Project DefaultTargets="Compile">`  
  
 Można określić więcej niż jeden domyślny element docelowy w `DefaultTargets` atrybut wyświetlania elementów docelowych w kolejności, a za pomocą średnika do rozdzielenia każdego obiektu docelowego. Obiekty docelowe, na liście będzie wykonywane sekwencyjnie.  
  
#### <a name="to-specify-more-than-one-default-target"></a>Aby określić więcej niż jeden cel domyślne  
  
-   Domyślne elementy docelowe, oddzielone średnikami w liście `DefaultTargets` atrybutu `Project` elementu. Na przykład, aby uruchomić `Clean` docelowego, a następnie `Compile` docelowych, wpisz:  
  
     `<Project DefaultTargets="Clean;Compile">`  
  
## <a name="using-the-target-switch"></a>Przy użyciu opcji/TARGET przełącznika  
 Jeśli docelowy domyślny nie jest zdefiniowany w pliku projektu lub jeśli nie chcesz używać domyślnego obiektu docelowego, można użyć przełącznika wiersza polecenia **/target** Aby określić inny element docelowy. Określono z elementów docelowych lub docelowe **/target** przełącznika są uruchamiane zamiast określone przez elementy docelowe `DefaultTargets` atrybutu. Obiekty docelowe w `InitialTargets` atrybut zawsze uruchamiany najpierw.  
  
#### <a name="to-use-a-target-other-than-the-default-target-first"></a>Umożliwia element docelowy inny niż domyślny obiekt docelowy  
  
-   Określ cel jako pierwszy przy użyciu docelowego **/target** przełącznik wiersza polecenia. Na przykład:  
  
     `msbuild file.proj /target:Clean`  
  
#### <a name="to-use-several-targets-other-than-the-default-targets-first"></a>Umożliwia kilku celów innych niż domyślne elementy docelowe  
  
-   Lista elementów docelowych, oddzielonych średnikami lub przecinkami, za pomocą **/target** przełącznik wiersza polecenia. Na przykład:  
  
     `msbuild <file name>.proj /t:Clean;Compile`  
  
## <a name="see-also"></a>Zobacz też
  [MSBuild](../msbuild/msbuild.md)  
 [Obiekty docelowe](../msbuild/msbuild-targets.md)   
 [Porady: czyszczenie kompilacji](../msbuild/how-to-clean-a-build.md)