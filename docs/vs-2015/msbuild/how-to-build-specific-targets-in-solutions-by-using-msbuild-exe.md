---
title: 'Porady: kompilacja określonych obiektów docelowych, w przypadku rozwiązań przy użyciu MSBuild.exe | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- MSBuild, building specific targets in a solution
- msbuild.exe, building specific targets in a solution
- MSBuild, msbuild.exe
ms.assetid: f46feb9b-4c16-4fec-b6e1-36a959692ba3
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: af1322145ad262a15b5ad47560e7c79aceeccc2b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49245846"
---
# <a name="how-to-build-specific-targets-in-solutions-by-using-msbuildexe"></a>Porady: kompilacja określonych obiektów docelowych w rozwiązaniach za pomocą programu MSBuild.exe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Można użyć MSBuild.exe, aby kompilacja określonych obiektów docelowych określonych projektów w rozwiązaniu.  
  
### <a name="to-build-a-specific-target-of-a-specific-project-in-a-solution"></a>Tworzenie konkretnego celu określonego projektu w rozwiązaniu  
  
1.  W wierszu polecenia wpisz polecenie `MSBuild.exe <SolutionName>.sln`, gdzie `<SolutionName>` odnosi się do nazwy pliku rozwiązania, który zawiera element docelowy, który chcesz wykonać.  
  
2.  Określ element docelowy po **/t** przełącznika w formacie *ProjectName*:*TargetName*.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład wykonuje `Rebuild` celem `NotInSlnFolder` projektu, a następnie wykonuje `Clean` celem `InSolutionFolder` projektu, który znajduje się w `NewFolder` folderu rozwiązania.  
  
```  
msbuild SlnFolders.sln /t:NotInSlnfolder:Rebuild;NewFolder\InSolutionFolder:Clean  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Informacje dotyczące wiersza polecenia](../msbuild/msbuild-command-line-reference.md)   
 [Odwołanie do narzędzia MSBuild](../msbuild/msbuild-reference.md)   
 [ Program MSBuild](msbuild.md)  
 [Pojęcia dotyczące programu MSBuild](../msbuild/msbuild-concepts.md)


