---
title: "Error — zadanie | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/msbuild/2003#Error
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Error task [MSBuild]
- MSBuild, Error task
ms.assetid: e96a90ee-a8ae-4e5b-8ef2-b5cf5fedd8b2
caps.latest.revision: "20"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 35360c057d0c18a1d6c891796f5788d5cfeab89b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="error-task"></a>Error — Zadanie
Zatrzymuje kompilację i rejestruje błąd oparte na obliczane instrukcji warunkowej.  
  
## <a name="parameters"></a>Parametry  
 W tabeli następujących opisano parametry `Error` zadań.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`Code`|Opcjonalne `String` parametru.<br /><br /> Kod błędu do skojarzenia z powodu błędu.|  
|`File`|Opcjonalne `String` parametru.<br /><br /> Nazwa pliku, który zawiera błąd. Jeśli zostanie podana żadna nazwa pliku, plik zawierający błąd zadań będzie używany.|  
|`HelpKeyword`|Opcjonalne `String` parametru.<br /><br /> Słowo kluczowe pomocy do skojarzenia z powodu błędu.|  
|`Text`|Opcjonalne `String` parametru.<br /><br /> Tekst błędu który [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] rejestruje Jeśli `Condition` daje w wyniku parametru `true`.|  
  
## <a name="remarks"></a>Uwagi  
 `Error` Zadanie pozwala [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] projektów wydać tekst błędu rejestratorów i zatrzymuje wykonywanie kompilacji.  
  
 Jeśli `Condition` daje w wyniku parametru `true`, kompilacja zostanie zatrzymana i jest rejestrowany błąd. Jeśli `Condition` parametr nie istnieje, błąd jest rejestrowany i zatrzymuje wykonywanie kompilacji. Aby uzyskać więcej informacji, zobacz [uzyskiwanie dzienników kompilacji](../msbuild/obtaining-build-logs-with-msbuild.md).  
  
 Oprócz wymienionych powyżej parametrów to zadanie dziedziczy parametrów z <xref:Microsoft.Build.Tasks.TaskExtension> dziedziczy klasa, która sama <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrach i ich opisy, zobacz [taskextension — klasa podstawowa](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu sprawdza, czy wszystkie wymagane właściwości są ustawione. Jeśli nie są ustawione, projekt wywołuje zdarzenie błędu i dzienniki wartość `Text` parametr `Error` zadań.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="ValidateCommandLine">  
        <Error  
            Text=" The 0 property must be set on the command line."  
            Condition="'$(0)' == ''" />  
        <Error  
            Text="The FREEBUILD property must be set on the command line."  
            Condition="'$(FREEBUILD)' == ''" />  
    </Target>  
    ...  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)   
 [Uzyskiwanie dzienników kompilacji](../msbuild/obtaining-build-logs-with-msbuild.md)