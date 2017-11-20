---
title: "Formatversion — zadanie | Dokumentacja firmy Microsoft"
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
ms.assetid: 96e692f6-b581-46ca-8cc9-441a1861e371
caps.latest.revision: "5"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: c74b737febc0fd91286abd4e4c43c5f84b9e6452
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="formatversion-task"></a>FormatVersion — Zadanie
Dołącza numer poprawki numer wersji.  
  
-   Przypadek #1: Dane wejściowe: wersja =\<Niezdefiniowany >;  Poprawki =\<nieważne >;   Dane wyjściowe: OutputVersion = "1.0.0.0"  
  
-   Przypadek #2: Dane wejściowe: wersja = "1.0.0.*" poprawkę = "5" w danych wyjściowych: OutputVersion = "1.0.0.5"  
  
-   Przypadek #3: Dane wejściowe: wersja = "1.0.0.0" poprawkę =\<nieważne >;  Dane wyjściowe: OutputVersion = "1.0.0.0"  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry `FormatVersion` zadań.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|`FormatType`|Opcjonalne `String` parametru.<br /><br /> Określa typ formatu.<br /><br /> -"Version" = wersja.<br />-"Path"= replace"." z "_";|  
|`OutputVersion`|Opcjonalne `String` parametru wyjściowego.<br /><br /> Określa wersję danych wyjściowych, zawierającą numer wersji.|  
|`Revision`|Opcjonalne `Int32` parametru.<br /><br /> Określa poprawkę do dołączenia do wersji.|  
|`Version`|Opcjonalne `String` parametru.<br /><br /> Określa ciąg numer wersji do formatowania.|  
  
## <a name="remarks"></a>Uwagi  
 Oprócz parametrów, które są wymienione w tabeli, to zadanie dziedziczy parametrów z <xref:Microsoft.Build.Tasks.TaskExtension> dziedziczy klasa, która sama <xref:Microsoft.Build.Utilities.Task> klasy. Aby uzyskać listę tych dodatkowych parametrach i ich opisy, zobacz [taskextension — klasa podstawowa](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Zadania](../msbuild/msbuild-tasks.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)