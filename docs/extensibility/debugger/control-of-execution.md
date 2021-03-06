---
title: Kontrola wykonywania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], control of execution
ms.assetid: 97071846-007e-450f-95a6-f072d0f5e61e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 42a95e01a44236d4f98f55f50a56cf28473ad575
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49927544"
---
# <a name="control-of-execution"></a>Kontrola wykonywania
Aparat debugowania (DE) zwykle wysyła jedno z następujących zdarzeń jako ostatnie zdarzenie uruchamiania:  
  
- Zdarzenie punktu wejścia, jeśli dołączanie do nowo wprowadzona na rynek programu  
  
- Pełne zdarzenie load, jeśli dołączanie do programu, który jest już uruchomiony  
  
  Zdarzenia te są zdarzeniami zatrzymującymi, co oznacza, że DE czeka na odpowiedź od użytkownika za pomocą środowiska IDE. Aby uzyskać więcej informacji, zobacz [tryby operacyjne](../../extensibility/debugger/operational-modes.md).  
  
## <a name="stopping-event"></a>Zatrzymywanie zdarzeń  
 Podczas zatrzymywania jest wysyłane zdarzenie sesję debugowania:  
  
1. Program i wątku, który zawiera bieżący wskaźnik instrukcji można uzyskać z interfejsu zdarzenia.  
  
2. IDE ustala bieżącego pliku kodu źródłowego i pozycji, które są wyświetlane jako wyróżniony w edytorze.  
  
3. Sesja debugowania zazwyczaj odpowiada na to pierwsze zdarzenie zatrzymywania, wywołując program **Kontynuuj** metody.  
  
4. Następnie program będzie uruchamiany, aż do napotkania zatrzymywanie warunek, np. Aktywacja punktu przerwania. W takim przypadku DE wysyła zdarzenie punktu przerwania sesji debugowania. Zdarzenie punktu przerwania jest zdarzeniem zatrzymywanie i DE ponownie czeka na odpowiedź użytkownika.  
  
5. Jeśli użytkownik wybiera Wkrocz ponad lub z funkcji, środowisko IDE wyświetla monit o sesji debugowania, aby wywołać program `Step` metody. IDE następnie przekazuje jednostki kroku (instrukcji, instrukcja lub wiersza) i typ kroku (czy krok do, nad lub poza funkcji). Po ukończeniu kroku DE wysyła zdarzenie ukończenia kroku do tej sesji debugowania, co jest zdarzenie zatrzymywania.  
  
    —lub—  
  
    Jeśli użytkownik wybiera kontynuowania wykonywania z bieżący wskaźnik instrukcji, IDE wyświetla monit o sesji debugowania, aby wywołać program **Execute** metody. Program wznawia wykonanie, aż do napotkania następnego stanu zatrzymywania.  
  
    —lub—  
  
    W przypadku sesji debugowania ignorowanie zdarzenia określonego zatrzymywania, sesja debugowania wywołuje program **Kontynuuj** metody. Jeśli program został przechodzenie krok po kroku do, nad lub poza funkcją gdy wystąpił warunek zatrzymywania, kontynuuje ten krok.  
  
   Programowo, DE napotka stan zatrzymywanie, wysyła takich zdarzeń Zatrzymywanie jako [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) lub [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) do Menedżer debugowania sesji (SDM) przez [IDebugEventCallback2](../../extensibility/debugger/reference/idebugeventcallback2.md) interfejsu. Przebiegi DE [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) i [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md) interfejsy, które reprezentują program i wątku, zawierające bieżący wskaźnik instrukcji. Wywołania SDM [IDebugThread2::EnumFrameInfo](../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md) ramki stosu w górnym i wywołania [IDebugStackFrame2::GetDocumentContext](../../extensibility/debugger/reference/idebugstackframe2-getdocumentcontext.md) pobrać kontekstu dokument skojarzony z bieżącej instrukcji wskaźnik. Ten kontekst dokumentu jest zazwyczaj źródła pliku nazwa, wierszy i kolumn numer kodu. IDE używa ich, aby wyróżnić kodu źródłowego, który zawiera bieżący wskaźnik instrukcji.  
  
   SDM zazwyczaj odpowiada to pierwsze zdarzenie zatrzymywania, wywołując [IDebugProgram2::Continue](../../extensibility/debugger/reference/idebugprogram2-continue.md). Program następnie działa aż do napotkania zatrzymywanie warunek, np. Aktywacja punktu przerwania, wysyła przypadek DE [interfejsu IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md) do SDM. Zdarzenie punktu przerwania jest zdarzeniem zatrzymywanie i DE ponownie czeka na odpowiedź użytkownika.  
  
   Jeśli użytkownik wybiera Wkrocz ponad lub z funkcji, środowisko IDE wyświetla monit o SDM wywołać [IDebugProgram2::Step](../../extensibility/debugger/reference/idebugprogram2-step.md). Następnie przekazuje IDE [STEPUNIT](../../extensibility/debugger/reference/stepunit.md) (instrukcji, instrukcja lub wiersza) i [STEPKIND](../../extensibility/debugger/reference/stepkind.md), oznacza to, czy krok do, nad lub poza funkcji. Po ukończeniu kroku DE wysyła [IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) interfejs SDM, czyli zdarzeń zatrzymywania.  
  
   Jeśli użytkownik wybiera kontynuowania wykonywania z bieżący wskaźnik instrukcji, IDE prosi SDM, aby wywołać [IDebugProgram2::Execute](../../extensibility/debugger/reference/idebugprogram2-execute.md). Program wznawia wykonanie, aż do napotkania następnego stanu zatrzymywania.  
  
   W przypadku pakietu debugowania ignorowanie zdarzenia określonego zatrzymywania, debugowanie pakietu wywołuje SDM, która wywołuje [IDebugProgram2::Continue](../../extensibility/debugger/reference/idebugprogram2-continue.md). Jeśli program został przechodzenie krok po kroku do, nad lub poza funkcją gdy wystąpił warunek zatrzymywania, kontynuuje ten krok. Oznacza to, że program przechowuje stan przechodzenia krok po kroku, tak aby wie, jak można kontynuować.  
  
   Wywołania SDM sprawia, że dla `Step`, **Execute**, i **Kontynuuj** czy asynchroniczny, co oznacza, że SDM oczekuje, że wywołanie szybko zwracać wynik. Jeśli DE wysyła SDM zdarzeń zatrzymywanie na tym samym wątku przed `Step`, **Execute**, lub **Kontynuuj** zwraca, SDM zawiesza się.  
  
## <a name="see-also"></a>Zobacz także  
 [Debugowanie zadań](../../extensibility/debugger/debugging-tasks.md)