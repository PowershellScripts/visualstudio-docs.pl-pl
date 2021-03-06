---
title: Findunderpath — zadanie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#FindUnderPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, FindUnderPath task
- FindUnderPath task [MSBuild]
ms.assetid: 3c6d58b0-36e8-47aa-bfca-b73dd2045d91
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a6ff04bad3f2f8c18175c8e96647fa1217c44725
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49198539"
---
# <a name="findunderpath-task"></a>FindUnderPath — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Określa, które elementy w kolekcji określonego elementu mają ścieżek, które znajdują się w lub pod określonym folderze.  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry `FindUnderPath` zadania.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`Files`|Opcjonalnie <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametru.<br /><br /> Określa pliki, których ścieżki powinny zostać porównane z ścieżka określona przez plik `Path` parametru.|  
|`InPath`|Opcjonalnie <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametr wyjściowy.<br /><br /> Zawiera elementy, które zostały znalezione w określonej ścieżce.|  
|`OutOfPath`|Opcjonalnie <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametr wyjściowy.<br /><br /> Zawiera elementy, które nie zostały odnalezione w określonej ścieżce.|  
|`Path`|Wymagane <xref:Microsoft.Build.Framework.ITaskItem> parametru.<br /><br /> Określa ścieżkę folderu, do użycia jako odwołanie.|  
|`UpdateToAbsolutePaths`|Opcjonalnie `Boolean` parametru.<br /><br /> W przypadku opcji true ścieżki elementów wyjściowych są zaktualizowane pod kątem ścieżek bezwzględnych.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz parametrów wymienionych powyżej, to zadanie dziedziczy parametry z <xref:Microsoft.Build.Tasks.TaskExtension> klasa, która sama dziedziczy <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrów i ich opisów, zobacz [taskextension — klasa bazowa](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie użyto `FindUnderPath` zadanie, aby określić, jeśli pliki zawarte w `MyFiles` elementów ma ścieżki, które istnieją w ścieżce określonej przez `SearchPath` właściwości. Po zakończeniu zadania, `FilesNotFoundInPath` element zawiera `File1.txt` pliku, a `FilesFoundInPath` element zawiera `File2.txt` pliku.  
  
```  
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



