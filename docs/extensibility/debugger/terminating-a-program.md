---
title: Kończenie programu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- programs, termination events
- debugging [Debugging SDK], terminating a program
ms.assetid: eedda0a3-5e05-44fe-841d-a2f4866ac72d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 29eb65f222a94816086e5b24b2579cbee0e48001
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49846255"
---
# <a name="terminating-a-program"></a>Kończenie programu
W poniższej sekcji opisano przed zakończeniem jednego programu z jednego wątku.  
  
## <a name="termination-process"></a>Zakończenie procesu  
  
1. Wysyła DE [IDebugThreadDestroyEvent2](../../extensibility/debugger/reference/idebugthreaddestroyevent2.md) przy użyciu prawidłowego [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md).  
  
2. Wysyła DE [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) przy użyciu prawidłowego [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md).  
  
   IDE przechodzi do trybu projektowania. Aparat debugowania lub wywołania w środowisku uruchomieniowym [IDebugPortNotify2::RemoveProgramNode](../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md) usunięcie programu z portu.  
  
## <a name="see-also"></a>Zobacz także  
 [Wywoływanie zdarzeń debugera](../../extensibility/debugger/calling-debugger-events.md)