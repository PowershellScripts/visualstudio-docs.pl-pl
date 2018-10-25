---
title: Taskbody — Element (MSBuild) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 03/13/2017
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- TaskBody element [MSBuild]
- <TaskBody> element [MSBuild]
ms.assetid: 49d8741b-f1ea-4470-94fd-a1ac27341a6a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4f0a3f24c5c8634301663f19dab9078bb37405b7
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49876558"
---
# <a name="taskbody-element-msbuild"></a>Taskbody — element (MSBuild)
Zawiera dane, które są przekazywane do `UsingTask` `TaskFactory`. Aby uzyskać więcej informacji, zobacz [usingtask — element (MSBuild)](../msbuild/usingtask-element-msbuild.md).  

 \<Project>  
 \<UsingTask>  
 \<Taskbody — >  

## <a name="syntax"></a>Składnia  

```xml
<TaskBody Evaluate="true/false" />  
```  

## <a name="attributes-and-elements"></a>Atrybuty i elementy  
 W poniższych sekcjach opisano atrybuty, elementy podrzędne i elementy nadrzędne.  

### <a name="attributes"></a>Atrybuty  

|Atrybut|Opis|  
|---------------|-----------------|  
|`Evaluate`|Opcjonalny logiczny atrybut.<br /><br /> Jeśli `true`, MSBuild ocenia wszelkie elementy wewnętrzne, a następnie rozwija elementów i właściwości przed przekazaniem informacje `TaskFactory` podczas konkretyzacji tego zadania.|  

### <a name="child-elements"></a>Elementy podrzędne  

|Element|Opis|  
|-------------|-----------------|  
|Dane|Tekst pomiędzy `TaskBody` znaczniki są wysyłane verbatim do `TaskFactory`.|  

### <a name="parent-elements"></a>Elementy nadrzędne  

| Element | Opis |
| - | - |
| [UsingTask](../msbuild/usingtask-element-msbuild.md) | Zapewnia sposób zarejestrować zadań w [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]. Może wynosić zero lub więcej `UsingTask` elementy w projekcie. |

## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak używać `TaskBody` element z `Evaluate` atrybutu.  

```xml  
<UsingTask TaskName="MyTask" AssemblyName="My.Assembly" TaskFactory="MyTaskFactory">  
       <ParameterGroup>  
              <Parameter1 ParameterType="System.String" Required="False" Output="False"/>  
              <Parameter2 ParameterType="System.Int" Required="True" Output="False"/>  
              ...  
</ParameterGroup>  
       <TaskBody Evaluate="true">  
      ... Task factory-specific data ...  
       </TaskBody>  
</UsingTask>  
```  

## <a name="see-also"></a>Zobacz także  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)   
 [Odwołanie do schematu pliku projektu](../msbuild/msbuild-project-file-schema-reference.md)
