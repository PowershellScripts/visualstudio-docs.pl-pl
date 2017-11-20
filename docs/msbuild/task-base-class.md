---
title: "Task — klasa podstawowa | Dokumentacja firmy Microsoft"
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
ms.assetid: 6c3f6238-b9f0-4325-b8b0-de61090bd0a2
caps.latest.revision: "6"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 8e8ef79fbbe619c4764c8f3abea5062d29159634
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="task-base-class"></a>Klasa podstawowa zadania
Wiele zadań, ale ostatecznie dziedziczyć <xref:Microsoft.Build.Utilities.Task> klasy. Ta klasa dodaje kilka parametrów do zadań, które pochodzi z nich. Te parametry są wymienione w niniejszym dokumencie.  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry klasy podstawowej.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|<xref:Microsoft.Build.Utilities.Task.BuildEngine%2A>|Opcjonalne <xref:Microsoft.Build.Framework.IBuildEngine> parametru.<br /><br /> Określa dostępne dla zadania interfejsu aparatu kompilacji. Ten parametr umożliwia zadań w celu wywołania zwrotnego do niego są automatycznie ustawiane w aparatu kompilacji.|  
|<xref:Microsoft.Build.Utilities.Task.BuildEngine2%2A>|Opcjonalne <xref:Microsoft.Build.Framework.IBuildEngine2> parametru.<br /><br /> Określa dostępne dla zadania interfejsu aparatu kompilacji. Ten parametr umożliwia zadań w celu wywołania zwrotnego do niego są automatycznie ustawiane w aparatu kompilacji.<br /><br /> Jest to właściwość wygody, aby autorzy zadań dziedziczenia z tej klasy nie należy rzutować wartości z `IBuildEngine` do `IBuildEngine2`.|  
|<xref:Microsoft.Build.Utilities.Task.BuildEngine3%2A>|Opcjonalne <xref:Microsoft.Build.Framework.IBuildEngine3> parametru.<br /><br /> Określa interfejs aparatu kompilacji dostarczony przez hosta.|  
|<xref:Microsoft.Build.Utilities.Task.HostObject%2A>|Opcjonalne <xref:Microsoft.Build.Framework.ITaskHost> parametru.<br /><br /> Określa wystąpienie obiektu hosta (może mieć wartości null). Aparat kompilacji ustawia tę właściwość, jeśli host IDE ma skojarzony obiekt hosta z tej konkretne zadanie.|  
|<xref:Microsoft.Build.Utilities.Task.Log%2A>|Opcjonalne <xref:Microsoft.Build.Utilities.TaskLoggingHelper> parametru tylko do odczytu.<br /><br /> Obiekt pomocnika rejestrowania.|  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)   
 [Zadania](../msbuild/msbuild-tasks.md)