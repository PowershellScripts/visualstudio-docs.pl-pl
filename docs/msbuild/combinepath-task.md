---
title: "Combinepath — zadanie | Dokumentacja firmy Microsoft"
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
- MSBuild, CombinePath task
- CombinePath task [MSBuild]
ms.assetid: c20edbf4-3d4f-4f66-b1d5-753a0d858ed8
caps.latest.revision: "7"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: ce45373667f1731753793306aa69556c46cceb86
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="combinepath-task"></a>CombinePath — Zadanie
Scala określonych ścieżek w pojedynczą ścieżkę.  
  
## <a name="task-parameters"></a>Parametry zadania  
 W poniższej tabeli opisano parametry [combinepath — zadanie](../msbuild/combinepath-task.md).  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`BasePath`|Wymagane `String` parametru.<br /><br /> Podstawowa ścieżka do łączenia z innych ścieżek. Może to być ścieżka względna, ścieżka bezwzględna lub pusty.|  
|`Paths`|Wymagany parametr interfejsu <xref:Microsoft.Build.Framework.ITaskItem>`[]`.<br /><br /> Lista poszczególnych ścieżek do łączenia z nieistniejący do utworzenia połączonym ścieżki. Ścieżki może być względna lub bezwzględna.|  
|`CombinedPaths`|Opcjonalne <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametru wyjściowego.<br /><br /> Połączone ścieżki, który jest tworzony przez to zadanie.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz wymienionych powyżej parametrów to zadanie dziedziczy parametrów z <xref:Microsoft.Build.Tasks.TaskExtension> dziedziczy klasa, która sama <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrach i ich opisy, zobacz [taskextension — klasa podstawowa](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)