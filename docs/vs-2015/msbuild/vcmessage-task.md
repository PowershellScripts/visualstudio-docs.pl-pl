---
title: Vcmessage — zadanie | Dokumentacja firmy Microsoft
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
- vc.task.vcmessage
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- VCMessage task (MSBuild (Visual C++))
- MSBuild (Visual C++), VCMessage task
ms.assetid: 956675fd-05dc-40b4-856f-616145103498
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f592160aae4fc1382b36c7331175eb6ab20d3fdc
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49243937"
---
# <a name="vcmessage-task"></a>VCMessage — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Dzienniki, ostrzeżenia i komunikaty o błędach podczas kompilacji.  
  
## <a name="remarks"></a>Uwagi  
 To zadanie ułatwia Implementowanie MSBuild dla języka Visual C++ i nie jest przeznaczona do wywoływania przez użytkownika. Aby uzyskać więcej informacji, zobacz <xref:Microsoft.Build.Utilities.TaskLoggingHelper>.  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry **vcmessage —** zadania.  
  
|Parametr|Opis|  
|---------------|-----------------|  
|**Argumenty**|Opcjonalnie **ciąg** parametru.<br /><br /> Rozdzielana średnikami lista wiadomości do wyświetlenia.|  
|**Kod**|Wymagane **ciąg** parametru.<br /><br /> Numer błędu, który kwalifikuje wiadomości.|  
|**Typ**|Opcjonalnie **ciąg** parametru.<br /><br /> Określa rodzaj komunikatów do emitowania. Wybierz opcję `"Warning"` do emitowania komunikat ostrzegawczy lub `"Error"` do emitowania komunikat o błędzie.|  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)



