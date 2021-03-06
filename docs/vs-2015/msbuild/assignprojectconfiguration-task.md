---
title: AssignProjectConfiguration, zadanie | Dokumentacja firmy Microsoft
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
ms.assetid: 09633a0b-8f6f-4aba-8058-7cb4d13ce2c0
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 57e513dc8b5cb914fd26f23b63e1a7e7d4908b76
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49290514"
---
# <a name="assignprojectconfiguration-task"></a>AssignProjectConfiguration — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
To zadanie akceptuje ciągi konfiguracji listy i przypisuje je do określonych projektów.  
  
## <a name="task-parameters"></a>Parametry zadania  
 W poniższej tabeli opisano parametry `AssignProjectConfiguration` zadania.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`SolutionConfigurationContents`|Opcjonalnie `string` parametr wyjściowy.<br /><br /> Zawiera ciąg znaków XML zawierający konfigurację projektu dla każdego projektu. Konfiguracje są przypisywane do nazwanych projektów.|  
|`DefaultToVcxPlatformMapping`|Opcjonalnie `string` parametr wyjściowy.<br /><br /> Zawiera rozdzieloną średnikami listę mapowań od nazw używanych platform<br /><br /> przez większość typów do tych używanych przez pliki.vcxproj.<br /><br /> Na przykład:<br /><br /> `"AnyCPU=Win32;X86=Win32;X64=X64"`|  
|`VcxToDefaultPlatformMapping`|Optional<br /><br /> `string` Parametr wyjściowy.<br /><br /> Zawiera rozdzieloną średnikami listę mapowań od nazw platform .vcxproj do platform używanych przez większość typów.<br /><br /> Na przykład:<br /><br /> `"Win32=AnyCPU;X64=X64"`|  
|`CurrentProjectConfiguration`|Opcjonalnie `string` parametr wyjściowy.<br /><br /> Zawiera konfigurację dla bieżącego projektu.|  
|`CurrentProjectPlatform`|Opcjonalnie `string` parametr wyjściowy.<br /><br /> Zawiera platformę dla bieżącego projektu.|  
|`OnlyReferenceAndBuildProjectsEnabledInSolutionConfiguration`|Opcjonalnie `bool` parametr wyjściowy.<br /><br /> Zawiera flagę wskazującą, czy odwołania powinny być tworzone, nawet jeśli zostały wyłączone w konfiguracji projektu.|  
|`ShouldUnsetParentConfigurationAndPlatform`|Opcjonalnie `bool` parametr wyjściowy.<br /><br /> Zawiera flagę wskazującą, jeśli konfiguracja nadrzędna i platforma powinny być nieustalone.|  
|`OutputType`|Opcjonalnie `string` parametr wyjściowy.<br /><br /> Zawiera typ danych wyjściowych dla projektu.|  
|`ResolveConfigurationPlatformUsingMappings`|Opcjonalnie `bool` parametr wyjściowy.<br /><br /> Zawiera flagę wskazującą, jeśli kompilacja powinna używać domyślnego mapowania do rozpoznawania konfiguracji i platformy przekazanych w odwołaniach projektu.|  
|`AssignedProjects`|Opcjonalnie <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametr wyjściowy.<br /><br /> Zawiera listę ścieżek rozpoznanych odwołań.|  
|`UnassignedProjects`|Opcjonalnie <xref:Microsoft.Build.Framework.ITaskItem> `[]` parametr wyjściowy.<br /><br /> Zawiera listę elementów odniesienia projektu, których nie można rozpoznać przy użyciu wstępnie rozpoznanej listy wyników.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz parametrów wymienionych powyżej, to zadanie dziedziczy parametry z <xref:Microsoft.Build.Tasks.TaskExtension> klasa, która sama dziedziczy <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrów i ich opisów, zobacz [taskextension — klasa bazowa](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)



