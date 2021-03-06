---
title: Kanały (Widok wątków) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.channelnames
helpviewer_keywords:
- Concurrency Visualizer, Channels (Threads View)
ms.assetid: 2f798c17-2363-42a4-be94-a5751d208eac
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 42b1baeec4543cb56d1e2320f26c9457dd7aac80
ms.sourcegitcommit: 209c2c068ff0975994ed892b62aa9b834a7f6077
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/17/2018
ms.locfileid: "34269131"
---
# <a name="channels-threads-view"></a>Kanały (Widok wątków)
Narzędzia Concurrency Visualizer przedstawiono cztery rodzaje kanałów: wątku kanały, kanały dysku znacznika kanałów i kanały procesora GPU.  
  
## <a name="thread-channels"></a>Kanały wątku  
 Kanał wątku pokazuje stan wątku przez kolor dla tylko jednego wątku. Po zatrzymaniu na nazwę kanału, zostanie wyświetlony funkcja start dla danego wątku. Narzędzia Concurrency Visualizer wykrywa kilka rodzajów wątków. W poniższej tabeli przedstawiono najbardziej typowych rodzajów.  
  
|||  
|-|-|  
|Wątku głównego|Wątek, który uruchomił aplikację.|  
|Wątek roboczy|Wątek, który został utworzony przez wątku głównego aplikacji.|  
|Wątek roboczy CLR|Wątek roboczy, która została utworzona przez środowisko uruchomieniowe języka wspólnego (CLR).|  
|Pomocnik debugera|Wątek roboczy, który został utworzony przez debuger programu Visual Studio.|  
|ConcRT wątku|Wątek, który został utworzony przez współbieżność środowiska wykonawczego Microsoft.|  
|Wątek interfejsu GDI|Wątek, który został utworzony przez GDIPlus.|  
|Wątek OLE/RPC|Wątek, który został utworzony jako wątku roboczego RPC.|  
|Wątek RPC|Wątek, który został utworzony jako wątek usługi RPC.|  
|Wątek Winsock|Wątek, który został utworzony jako wątek interfejsu Winsock.|  
|Pula wątków|Wątek, który został utworzony w puli wątków CLR.|  
  
## <a name="disk-channels"></a>Kanały dysku  
 Kanały dysku odpowiadają dysków fizycznych w komputerze. Każdego dysku, ponieważ istnieje osobny kanał dla operacji odczytu i zapisu dla każdego dysku fizycznego w systemie, ma dwa kanały. Numery dysków odpowiadają nazwy urządzeń jądra. Kanał dysku jest wyświetlany tylko jeśli na dysku został działania.  
  
## <a name="marker-channels"></a>Kanały znacznika  
 Kanały znacznika odpowiadają zdarzeń generowanych przez aplikację i bibliotek, które są używane. Na przykład biblioteka zadań równoległych, biblioteka równoległych wzorców i C++ AMP generowanie zdarzeń, które są wyświetlane jako znaczniki. Każdy znacznik kanał jest skojarzony z Identyfikatorem wątku, który jest wyświetlany obok opis kanału. Identyfikator identyfikuje wątku, który wygenerował zdarzenie. Opis kanału zawiera nazwę dostawcy funkcji Śledzenie zdarzeń systemu Windows (), który wygenerował zdarzenia. Jeśli kanał Wyświetla zdarzenia z [SDK wizualizatora współbieżności](../profiling/concurrency-visualizer-sdk.md), jest również wyświetlana nazwa serii.  
  
## <a name="gpu-channels"></a>Kanały procesora GPU  
 Kanały GPU zawierają informacje dotyczące działania programu DirectX 11, w systemie.  Aparat programu DirectX, każdy skojarzoną z karty graficznej ma oddzielny kanał.  Poszczególnych segmentów odpowiadają za czas, który ma poświęcony na przetwarzanie pakietów DMA.  
  
## <a name="see-also"></a>Zobacz także  
 [Widok wątków](../profiling/threads-view-parallel-performance.md)