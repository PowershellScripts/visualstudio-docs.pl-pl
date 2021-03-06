---
title: QueryCounters | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 8059d4b2-af61-4a47-a6c2-8da5c0741c74
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9f3c3176ea0b865ecf4a433a7a0a22a316720229
ms.sourcegitcommit: 34f7d23ce3bd140dcae875b602d5719bb4363ed1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35257712"
---
# <a name="querycounters"></a>QueryCounters
**QueryCounters** opcja Wyświetla liczniki wydajności procesora CPU (sprzęt), które są dostępne na komputerze.  
  
 **QueryCounters** musi być jedyną opcją w wierszu polecenia.  
  
## <a name="syntax"></a>Składnia  
  
```cmd  
VSPerfCmd.exe /QueryCounters  
```  
  
#### <a name="parameters"></a>Parametry  
 Brak  
  
## <a name="remarks"></a>Uwagi  
 Jeśli używasz metody Instrumentacji profilera mogą zbierać wartości co najmniej jeden liczniki wydajności procesora CPU na każdego zdarzenia zbierania danych. Gdy używana jest metoda profilowania próbkowania, można określić jeden licznik zdarzeń i liczbę wystąpień zdarzeń ma być używany jako interwał próbkowania.  
  
 Różnych procesorów ujawnić różne liczniki wydajności procesora CPU. Profiler definiuje zestaw ogólnego liczniki, które mogą być używane w prawie wszystkie procesory. **QueryCounters** opcja wyświetla zarówno nazw liczników ogólnego i nazwy liczników, które są specyficzne dla procesora.  
  
## <a name="see-also"></a>Zobacz także  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profil aplikacji autonomicznych](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Aplikacje sieci web ASP.NET profilu](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Usługi profilowania](../profiling/command-line-profiling-of-services.md)