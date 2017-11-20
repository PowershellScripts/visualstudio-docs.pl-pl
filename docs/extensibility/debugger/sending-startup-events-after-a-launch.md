---
title: "Wysyłanie zdarzeń do uruchomienia po Launch | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: debugging [Debugging SDK], startup events
ms.assetid: 306ea0b4-6d9e-4871-8d8d-a4032d422940
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0620821ec908deed2c57ddfefb40763a48fd2074
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="sending-startup-events-after-a-launch"></a>Wysyłanie zdarzeń do uruchomienia po Launch
Gdy aparat debugowania (DE) jest dołączony do programu, szereg zdarzenia uruchamiania wysyłane z powrotem do sesji debugowania.  
  
 Następujące zdarzenia uruchamiania wysyłane z powrotem do sesji debugowania:  
  
-   Aparat tworzenia zdarzenia.  
  
-   Zdarzenie tworzenia programu.  
  
-   Wątek, tworzenie i zdarzeń ładowania modułu.  
  
-   Zdarzenie complete obciążenia, wysyłane, jeśli kod jest załadowany i gotowa do uruchomienia, ale przed wykonaniem żadnego kodu  
  
    > [!NOTE]
    >  Gdy to zdarzenie jest kontynuowane, zmienne globalne są inicjowane i uruchamianie procedury uruchamiania.  
  
-   Możliwe innych wątków, tworzenie i zdarzeń ładowania modułu.  
  
-   Zdarzenie punktu wejścia, która sygnalizuje, że program została osiągnięta jego główny punkt wejścia, takich jak **Main** lub `WinMain`. To zdarzenie nie są zwykle wysyłane Jeśli DE dołącza do programu, który jest już uruchomiony.  
  
 Programowo, DE najpierw wysyła Menedżera debugowania sesji (SDM) [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) interfejsu reprezentuje aparatu tworzenia zdarzeń, a następnie [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) , która reprezentuje zdarzenie tworzenia programu.  
  
 To jest zazwyczaj następuje co najmniej jeden [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) zdarzenia Tworzenie wątków i [IDebugModuleLoadEvent2](../../extensibility/debugger/reference/idebugmoduleloadevent2.md) zdarzeń ładowania modułu.  
  
 Jeśli kod jest załadowany i gotowa do uruchomienia, ale przed wykonaniem dowolny kod DE wysyła SDM [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) zdarzenie ukończenia ładowania. Na koniec, jeśli program nie jest już uruchomiony, wysyła DE [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) zdarzenie punktu wejścia, sygnalizowania, że program osiągnął swoją główny punkt wejścia i jest gotowy do debugowania.  
  
## <a name="see-also"></a>Zobacz też  
 [Kontrola wykonywania](../../extensibility/debugger/control-of-execution.md)   
 [Debugowanie zadań](../../extensibility/debugger/debugging-tasks.md)