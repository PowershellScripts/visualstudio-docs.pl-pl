---
title: Wysyłanie wymaganych zdarzeń | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], required events
ms.assetid: 08319157-43fb-44a9-9a63-50b919fe1377
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 2512dc35d77263c5237dff12b7a5f07060458e1c
ms.sourcegitcommit: 71b307ce86c4079cc7ad686d8d5f96a6a123aadd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/25/2018
ms.locfileid: "39251426"
---
# <a name="send-the-required-events"></a>Wysyłanie wymaganych zdarzeń
Użyj tej procedury związane z przesyłaniem zdarzeń wymagane.  
  
## <a name="process-for-sending-required-events"></a>Proces wysyłanie wymaganych zdarzeń  
 Następujące zdarzenia są wymagane w następującej kolejności podczas tworzenia debugowania aparatu (DE) i dołączania ich do programu:  
  
1.  Wyślij [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) obiekt zdarzenia do Menedżer debugowania sesji (SDM) DE jest inicjowany do jednego lub wielu programów w procesie debugowania.  
  
2.  Gdy program ma być debugowany jest dołączony do, Wyślij [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) obiekt zdarzenia do SDM. To zdarzenie może być to zdarzenie zatrzymywania, w zależności od projektu aparatu.  
  
3.  Jeśli program jest dołączony do, gdy proces jest uruchamiany, Wyślij [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) obiekt zdarzenia do SDM, by powiadomić IDE nowy wątek. To zdarzenie może być to zdarzenie zatrzymywania, w zależności od projektu aparatu.  
  
4.  Wyślij [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) obiekt zdarzenia do SDM po debugowanego Zakończono ładowania lub po wykonaniu dołączanie do programu. To zdarzenie musi być zdarzeń zatrzymywania.  
  
5.  Jeśli nie uruchomiono aplikacji przeznaczonej do debugowania, Wyślij [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) obiekt zdarzenia do SDM, gdy pierwsza instrukcja kodu w architekturze środowiska wykonawczego ma zostać wykonana. To zdarzenie jest zawsze zdarzeń zatrzymywania. Po przejściu do sesji debugowania, IDE zatrzymuje się na to zdarzenie.  
  
> [!NOTE]
>  Wiele języków użycia inicjatorów globalnych lub zewnętrznymi, wstępnie skompilowanych funkcji (od biblioteki CRT lub _Main) na początku swój kod. Jeśli język programu debugowania zawierają dowolne z tych typów elementów przed punktu wejścia początkowej, ten kod jest uruchamiany i jest wysyłane zdarzenie punktu wejścia po użytkownik punkt wejścia, takich jak **głównego** lub `WinMain`, jest osiągnięta.  
  
## <a name="see-also"></a>Zobacz także  
 [Włączanie programu do debugowania](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)