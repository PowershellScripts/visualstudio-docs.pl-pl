---
title: Wysyłanie wymaganych zdarzeń | Dokumentacja firmy Microsoft
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
- debugging [Debugging SDK], required events
ms.assetid: 08319157-43fb-44a9-9a63-50b919fe1377
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 154157a8de67cd1bef8fd489b3c1fc7406a05629
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49303674"
---
# <a name="sending-the-required-events"></a>Wysyłanie wymaganych zdarzeń
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Użyj tej procedury związane z przesyłaniem zdarzeń wymagane.  
  
## <a name="process-for-sending-required-events"></a>Proces wysyłanie wymaganych zdarzeń  
 Następujące zdarzenia są wymagane w następującej kolejności podczas tworzenia debugowania aparatu (DE) i dołączania ich do programu:  
  
1.  Wyślij [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) obiekt zdarzenia do Menedżer debugowania sesji (SDM) DE jest inicjowany do jednego lub wielu programów w procesie debugowania.  
  
2.  Gdy program ma być debugowany jest dołączony do, Wyślij [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) obiekt zdarzenia do SDM. To zdarzenie może być to zdarzenie zatrzymywania, w zależności od projektu aparatu.  
  
3.  Jeśli program jest dołączony do, gdy proces jest uruchamiany, Wyślij [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) obiekt zdarzenia do SDM, by powiadomić IDE nowy wątek. To zdarzenie może być to zdarzenie zatrzymywania, w zależności od projektu aparatu.  
  
4.  Wyślij [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) obiekt zdarzenia do SDM po debugowanego Zakończono ładowania lub po wykonaniu dołączanie do programu. To zdarzenie musi być zdarzeń zatrzymywania.  
  
5.  Jeśli nie uruchomiono aplikacji przeznaczonej do debugowania, Wyślij [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) obiekt zdarzenia do SDM, gdy pierwsza instrukcja kodu w architekturze środowiska wykonawczego ma zostać wykonana. To zdarzenie jest zawsze zdarzeń zatrzymywania. Po przejściu do sesji debugowania, IDE zatrzymuje się na to zdarzenie.  
  
> [!NOTE]
>  Wiele języków użycia inicjatorów globalnych lub zewnętrznymi, wstępnie skompilowanych funkcji (od biblioteki CRT lub _Main) na początku swój kod. Jeśli język programu debugowania zawierają dowolne z tych typów elementów przed punktu wejścia początkową, a następnie uruchamiać ten kod i jest wysyłane zdarzenie punktu wejścia po użytkownik punkt wejścia, takich jak **głównego** lub `WinMain`, zostanie osiągnięty.  
  
## <a name="see-also"></a>Zobacz też  
 [Włączanie debugowania programu](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)

