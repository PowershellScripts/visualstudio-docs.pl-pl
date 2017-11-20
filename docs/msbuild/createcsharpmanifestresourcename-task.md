---
title: "Createcsharpmanifestresourcename — zadanie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, CreateCSharpManifestResourceName task
- CreateCSharpManifestResourceName task [MSBuild]
ms.assetid: 2ace88c1-d757-40a7-8158-c1d3f5ff0511
caps.latest.revision: "8"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 9d18d7809357c8f4fa7bce796e7f05981a0f8c99
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="createcsharpmanifestresourcename-task"></a>CreateCSharpManifestResourceName — Zadanie
Tworzy [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)]— styl nazwy manifestu z nazwę pliku .resx danego lub innego zasobu.  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry [createcsharpmanifestresourcename — zadanie](../msbuild/createcsharpmanifestresourcename-task.md).  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`ManifestResourceNames`|<xref:Microsoft.Build.Framework.ITaskItem>`[]` tylko do odczytu parametru wyjściowego.<br /><br /> Wynikowa nazwy manifestu.|  
|`ResourceFiles`|Wymagane `String` parametru.<br /><br /> Nazwa pliku zasobu, z którym ma zostać utworzony [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] nazwę pliku manifestu.|  
|`RootNamespace`|Opcjonalne `String` parametru.<br /><br /> Główna przestrzeń nazw pliku zasobu, zazwyczaj pobierana z pliku projektu. Może być `null`.|  
|`PrependCultureAsDirectory`|Opcjonalne `Boolean` parametru.<br /><br /> Jeśli `true`, nazwa kultury jest dodawana jako nazwę katalogu, bezpośrednio przed nazwy zasobu manifestu. Wartość domyślna to `true`.|  
|`ResourceFilesWithManifestResourceNames`|Opcjonalnie tylko do odczytu `String` parametru wyjściowego.<br /><br /> Zwraca nazwę pliku zasobu, która zawiera teraz nazwę zasobu manifestu.|  
  
## <a name="remarks"></a>Uwagi  
 [Createvisualbasicmanifestresourcename — zadanie](../msbuild/createvisualbasicmanifestresourcename-task.md) Określa nazwę zasobu manifestu odpowiednie do przypisania do .resx danego pliku lub innego zasobu. Zadanie zawiera nazwę logiczną do pliku zasobów i dołącza go do parametru wyjściowego jak metadanych.  
  
 Oprócz wymienionych powyżej parametrów to zadanie dziedziczy parametrów z <xref:Microsoft.Build.Tasks.TaskExtension> dziedziczy klasa, która sama <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrach i ich opisy, zobacz [taskextension — klasa podstawowa](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)