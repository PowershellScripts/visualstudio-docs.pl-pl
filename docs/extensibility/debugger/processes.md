---
title: Procesy | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], processes
ms.assetid: a6a1efdc-b243-40c8-a778-6f69f6b018be
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: df35a6e1614b558f7b94c24956e2dcdbc676a9e5
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49927147"
---
# <a name="processes"></a>Procesy
W architekturze debugera *procesu*:  
  
- To kontener dla zestawu programów. Jest ściśle analogiczne do procesu Windows, który jest kontenerem dla zestawu wątków.  
  
- Można zidentyfikować sama nazwa, identyfikator lub identyfikator fizycznych.  
  
- Można wyliczyć wszystkie uruchomione programy (i ich wątków).  
  
- Można opisać, port, na którym jest uruchomiona w i komputer który go zawiera.  
  
- Można utworzyć jeden lub więcej programów zakończenie dowolnych programów, które tworzy i spowodować, że program przestanie.  
  
- Jest reprezentowany przez [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md) interfejs, który jest tworzony, gdy proces jest uruchamiany. Proces jest uruchamiany przez albo Menedżer debugowania sesji (SDM) lub [LaunchSuspended](../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md).  
  
  Pakiet debugowania można dołączyć aparat debugowania (DE) do procesu przez wywołanie metody [Dołącz](../../extensibility/debugger/reference/idebugprocess2-attach.md), co oznacza, że Niemcy dołącza wszystkie możliwe programy działający w procesie, który może obsługiwać. Na przykład jeśli środowisko uruchomieniowe języka wspólnego DE dołącza do procesu, dołącza tylko do programów uruchomionych w kodzie zarządzanym.  
  
## <a name="see-also"></a>Zobacz także  
 [Programy](../../extensibility/debugger/programs.md)   
 [Wątki](../../extensibility/debugger/threads.md)   
 [Pojęcia dotyczące debugera](../../extensibility/debugger/debugger-concepts.md)   
 [Pakiet debugowania](../../extensibility/debugger/debug-package.md)   
 [Aparat debugowania](../../extensibility/debugger/debug-engine.md)   
 [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md)   
 [LaunchSuspended](../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)   
 [Attach](../../extensibility/debugger/reference/idebugprocess2-attach.md)