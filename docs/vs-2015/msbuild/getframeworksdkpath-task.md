---
title: Getframeworksdkpath — zadanie | Dokumentacja firmy Microsoft
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
- http://schemas.microsoft.com/developer/msbuild/2003#GetFrameworkSdkPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- GetFrameworkSdkPath task [MSBuild]
- MSBuild, GetFrameworkSdkPath task
ms.assetid: 2ef82b98-02b6-40cf-a9b5-f0e882fb5064
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1ca047d35ec914833d2044cb2ae9fd4f7cf322a6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49301785"
---
# <a name="getframeworksdkpath-task"></a>GetFrameworkSdkPath — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Pobiera ścieżkę do [!INCLUDE[winsdklong](../includes/winsdklong-md.md)].  
  
## <a name="task-parameters"></a>Parametry zadania  
 W poniższej tabeli opisano parametry `GetFrameworkSdkPath` zadania.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`FrameworkSdkVersion20Path`|Opcjonalnie `String` parametru wyjściowego tylko do odczytu.<br /><br /> Zwraca ścieżkę do zestawu SDK platformy .NET w wersji 2.0, jeśli jest obecny. W przeciwnym razie zwraca `String.Empty`.|  
|`FrameworkSdkVersion35Path`|Opcjonalnie `String` parametru wyjściowego tylko do odczytu.<br /><br /> Zwraca ścieżkę do zestawu SDK platformy .NET w wersji 3.5, jeśli jest obecny. W przeciwnym razie zwraca `String.Empty`.|  
|`FrameworkSdkVersion40Path`|Opcjonalnie `String` parametru wyjściowego tylko do odczytu.<br /><br /> Zwraca ścieżkę do zestawu SDK platformy .NET w wersji 4.0, jeśli jest obecny. W przeciwnym razie zwraca `String.Empty`.|  
|`Path`|Opcjonalnie `String` parametr wyjściowy.<br /><br /> Zawiera ścieżkę do najnowszy zestaw SDK platformy .NET, jeśli dowolna wersja jest obecny. W przeciwnym razie zwraca `String.Empty`.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz parametrów wymienionych powyżej, to zadanie dziedziczy parametry z <xref:Microsoft.Build.Tasks.TaskExtension> klasa, która sama dziedziczy <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrów i ich opisów, zobacz [taskextension — klasa bazowa](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie użyto `GetFrameworkSdkPath` zadania do ścieżki do przechowywania [!INCLUDE[winsdkshort](../includes/winsdkshort-md.md)] w `SdkPath` właściwości.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="GetPath">  
        <GetFrameworkSdkPath>  
            <Output  
                TaskParameter="Path"  
                PropertyName="SdkPath" />  
        </GetFrameworkSdkPath>  
        <Message Text="$(SdkPath)"/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)



