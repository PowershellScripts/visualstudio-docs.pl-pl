---
title: Warning — zadanie | Dokumentacja firmy Microsoft
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
- http://schemas.microsoft.com/developer/msbuild/2003#Warning
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Warning task [MSBuild]
- MSBuild, Warning task
ms.assetid: 96ba5507-8b43-4f54-a1d7-9b15644dd56c
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0447c3803de6845dcfb02a30270cfe9b96b96f0a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49213601"
---
# <a name="warning-task"></a>Warning — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Dzienniki ostrzeżenie podczas kompilacji w oparciu ocenianą instrukcji warunkowej.  
  
## <a name="parameters"></a>Parametry  
 W następujących tabeli przedstawiono parametry `Warning` zadania.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`Code`|Opcjonalnie `String` parametru.<br /><br /> Kod ostrzegawczy do skojarzenia z ostrzeżeniem.|  
|`File`|Opcjonalnie `String` parametru.<br /><br /> Określa odpowiedni plik, jeśli istnieje. Jeśli plik nie zostanie podana, zostanie użyty plik zawierający ostrzeżenie zadanie.|  
|`HelpKeyword`|Opcjonalnie `String` parametru.<br /><br /> Słowo kluczowe pomocy do skojarzenia z ostrzeżeniem.|  
|`Text`|Opcjonalnie `String` parametru.<br /><br /> Tekst ostrzeżenia, [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] rejestruje Jeśli `Condition` daje w wyniku parametru `true`.|  
  
## <a name="remarks"></a>Uwagi  
 `Warning` Zadanie pozwala [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] krok kompilacji projektów pod kątem obecności wymaganej konfiguracji lub właściwości przed przejściem dalej.  
  
 Jeśli `Condition` parametru `Warning` daje w wyniku zadania `true`, wartość `Text` parametru jest rejestrowana i kontynuuje wykonywanie kompilacji. Jeśli `Condition` parametru nie nie exisit, tekst ostrzeżenia jest rejestrowane. Aby uzyskać więcej informacji na temat rejestrowania, zobacz [uzyskiwanie dzienników kompilacji](../msbuild/obtaining-build-logs-with-msbuild.md).  
  
 Oprócz parametrów wymienionych powyżej, to zadanie dziedziczy parametry z <xref:Microsoft.Build.Tasks.TaskExtension> klasa, która sama dziedziczy <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrów i ich opisów, zobacz [taskextension — klasa bazowa](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu sprawdza właściwości, które są ustawiane w wierszu polecenia. W przypadku nie ustawiono właściwości projektu wywołuje zdarzenie ostrzegawcze i rejestruje wartość `Text` parametru `Warning` zadania.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="ValidateCommandLine">  
        <Warning  
            Text=" The 0 property was not set on the command line."  
            Condition="'$(0)' == ''" />  
        <Warning  
            Text=" The FREEBUILD property was not set on the command line."  
            Condition="'$(FREEBUILD)' == ''" />  
    </Target>  
    ...  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Uzyskiwanie dzienników kompilacji](../msbuild/obtaining-build-logs-with-msbuild.md)   
 [Odwołanie do schematu pliku projektu](../msbuild/msbuild-project-file-schema-reference.md)



