---
title: "Findunderpath — zadanie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/msbuild/2003#FindUnderPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, FindUnderPath task
- FindUnderPath task [MSBuild]
ms.assetid: 3c6d58b0-36e8-47aa-bfca-b73dd2045d91
caps.latest.revision: "9"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: fcb43188414df57bd3c41286ca7e3d3caa8718d5
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="findunderpath-task"></a>FindUnderPath — Zadanie
Określa, które elementy w kolekcji określony element mają ścieżek, które znajdują się w lub poniżej określonego folderu.  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry `FindUnderPath` zadań.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`Files`|Opcjonalne <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametru.<br /><br /> Określa pliki, których ścieżki powinny zostać porównane z ścieżka określona przez `Path` parametru.|  
|`InPath`|Opcjonalne <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametru wyjściowego.<br /><br /> Zawiera elementy, które zostały odnalezione w określonej ścieżce.|  
|`OutOfPath`|Opcjonalne <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametru wyjściowego.<br /><br /> Zawiera elementy, które nie zostały odnalezione w określonej ścieżce.|  
|`Path`|Wymagane <xref:Microsoft.Build.Framework.ITaskItem> parametru.<br /><br /> Określa ścieżkę do folderu do użycia jako punkt odniesienia.|  
|`UpdateToAbsolutePaths`|Opcjonalne `Boolean` parametru.<br /><br /> Jeśli PRAWDA, ścieżki elementów wyjściowych są aktualizowane za ścieżek bezwzględnych.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz wymienionych powyżej parametrów to zadanie dziedziczy parametrów z <xref:Microsoft.Build.Tasks.TaskExtension> dziedziczy klasa, która sama <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrach i ich opisy, zobacz [taskextension — klasa podstawowa](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie użyto `FindUnderPath` zadań w celu ustalenia, czy pliki zawarte w `MyFiles` elementu ma ścieżek, które istnieją w ścieżce określonej przez `SearchPath` właściwości. Po ukończeniu zadania, `FilesNotFoundInPath` element zawiera `File1.txt` pliku i `FilesFoundInPath` element zawiera `File2.txt` pliku.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemGroup>  
        <MyFiles Include="C:\File1.txt" />  
        <MyFiles Include="C:\Projects\MyProject\File2.txt" />  
    </ItemGroup>  
  
    <PropertyGroup>  
        <SearchPath>C:\Projects\MyProject</SearchPath>  
    </PropertyGroup>  
  
    <Target Name="FindFiles">  
        <FindUnderPath  
            Files="@(MyFiles)"  
            Path="$(SearchPath)">  
            <Output  
                TaskParameter="InPath"  
                ItemName="FilesFoundInPath" />  
            <Output  
                TaskParameter="OutOfPath"  
                ItemName="FilesNotFoundInPath" />  
        </FindUnderPath>  
    </Target>  
  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)   
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Pojęcia dotyczące programu MSBuild](../msbuild/msbuild-concepts.md)