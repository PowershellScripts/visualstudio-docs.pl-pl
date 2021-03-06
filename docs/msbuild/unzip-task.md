---
title: Rozpakuj zadań | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology: msbuild
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Unzip
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Unzip task [MSBuild]
- MSBuild, Unzip task
ms.assetid: 916bb2e3-3017-4828-ae27-c0b5c99bbb48
caps.latest.revision: 16
author: Mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f633e741cf72596708963d89973eb039b18b4e88
ms.sourcegitcommit: 0e5289414d90a314ca0d560c0c3fe9c88cb2217c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/19/2018
ms.locfileid: "39151216"
---
# <a name="unzip-task"></a>Rozpakuj zadania
Unzips *zip* archiwum do określonej lokalizacji.

>[!NOTE]
>`Unzip` Zadanie jest dostępne w MSBuild 15.8 i nowszym tylko.
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry `Unzip` zadania.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`DestinationFolder`|Wymagane <xref:Microsoft.Build.Framework.ITaskItem> parametru<br /><br /> Określa folder docelowy, aby rozpakować plik.|
|`OverwriteReadOnlyFiles`|Opcjonalnie `Boolean` parametru.<br /><br /> Jeśli `true`, zastępuje pliki tylko do odczytu. Wartość domyślna to `false`.|
|`SkipUnchangedFiles`|Opcjonalnie `Boolean` parametru.<br /><br /> Jeśli `true`, pomija Rozpakowywanie plików, które nie uległy zmianie. Wartość domyślna to `true`. Zadanie `Unzip` uznaje pliki za niezmienione, jeśli mają taki sam rozmiar i taki sam czas ostatniej modyfikacji.|
|`SourceFiles`|Wymagany parametr interfejsu <xref:Microsoft.Build.Framework.ITaskItem>`[]`.<br /><br /> Określa jeden lub więcej plików do rozpakowania. Podczas określania wielu plików, są one rozpakowany w kolejności, w tym samym folderze.|
  
## <a name="remarks"></a>Uwagi  
 Oprócz parametrów wymienionych powyżej, to zadanie dziedziczy parametry z <xref:Microsoft.Build.Tasks.TaskExtension> klasa, która sama dziedziczy <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrów i ich opisów, zobacz [taskextension — klasa bazowa](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Przykład  
 Poniższy przykład unzips archiwum i zastępuje wszystkie pliki tylko do odczytu.
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <Target Name="UnzipArchive" BeforeTargets="Build">
        <Unzip
            SourceFiles="MyArchive.zip"
            DestinationFolder="$(OutputPath)\unzipped"
            OverwriteReadOnlyFiles="true"
        />
    </Target>

</Project>
```
  
## <a name="see-also"></a>Zobacz także  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)
