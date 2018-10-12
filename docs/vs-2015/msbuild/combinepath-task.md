---
title: Combinepath — zadanie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
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
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 71176722443cc2e7f858bbfea85d526a4f4d772d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49192689"
---
# <a name="combinepath-task"></a>CombinePath — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Łączy określonych ścieżek w pojedynczą ścieżkę.  
  
## <a name="task-parameters"></a>Parametry zadania  
 W poniższej tabeli opisano parametry [combinepath — zadanie](../msbuild/combinepath-task.md).  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`BasePath`|Wymagane `String` parametru.<br /><br /> Ścieżki podstawowej, aby połączyć się z innych ścieżek. Może być ścieżką względną, ścieżka bezwzględna lub pusty.|  
|`Paths`|Wymagany parametr interfejsu <xref:Microsoft.Build.Framework.ITaskItem>`[]`.<br /><br /> Lista poszczególnych ścieżek do łączenia z BasePath do utworzenia złożonej ścieżki. Ścieżki mogą być względna lub bezwzględna.|  
|`CombinedPaths`|Opcjonalnie <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametr wyjściowy.<br /><br /> Połączone ścieżki, który jest tworzony przez to zadanie.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz parametrów wymienionych powyżej, to zadanie dziedziczy parametry z <xref:Microsoft.Build.Tasks.TaskExtension> klasa, która sama dziedziczy <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrów i ich opisów, zobacz [taskextension — klasa bazowa](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)



