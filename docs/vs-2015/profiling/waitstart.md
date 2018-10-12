---
title: WaitStart | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6c737177-2dfb-4150-963e-a49ac9aaa591
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a9f111ae1aed079f0c0cc0d94a1d1da7c8557e76
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49285912"
---
# <a name="waitstart"></a>WaitStart
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Opcja WaitStart powoduje, że podpolecenie VSPerfCmd.exe Start zwrócić tylko wtedy, gdy program profilujący został zainicjowany lub po upływie określonej liczby sekund. Domyślnie polecenia uruchomienia zwraca natychmiast. Jeśli polecenie podrzędne uruchamiania jest zwracane bez Inicjowanie programu profilującego, zwracany jest błąd. Jeśli nie określono liczbę sekund, przez czas nieokreślony oczekuje polecenia uruchomienia.  
  
 Opcja WaitStart przydaje się w plikach wsadowych, aby upewnić się, że ten program profilujący został zainicjowany.  
  
## <a name="syntax"></a>Składnia  
  
```  
VSPerfCmd.exe /Start:Method /Output:FileName[Options] /StartWait[:Seconds]  
```  
  
#### <a name="parameters"></a>Parametry  
 `Seconds`  
 Liczba sekund oczekiwania przed powrotem z podpolecenie rozpoczęcia.  
  
## <a name="required-options"></a>Wymagane opcje  
 Opcja WaitStart należy używać tylko za pomocą polecenia Start podrzędnych.  
  
 **Dane wyjściowe:** `filename`  
 Określa nazwę pliku wyjściowego.  
  
## <a name="remarks"></a>Uwagi  
  
## <a name="example"></a>Przykład  
 W tym przykładzie plik wsadowy polecenia uruchomienia będzie czekać na 5 sekund w celu na zainicjowanie programu profiler.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /WaitStart:5  
if not %errorlevel% 0 goto :error_tag  
VSPerfCmd.exe /Launch:TestApp.exe  
goto :end  
:error_tag  
@echo Could not start Profiler!  
@echo Error %errorlevel%  
:end  
```



