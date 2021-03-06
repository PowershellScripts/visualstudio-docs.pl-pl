---
title: Wyłączanie debugera Just In Time | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 05/23/18
ms.technology: vs-ide-debug
ms.topic: troubleshooting
helpviewer_keywords:
- debugging [Visual Studio], Just-In-Time
- Just-In-Time debugging
ms.assetid: 14972d5f-69bc-479b-9529-03b8787b118f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 147e16bab14a6a038622804cf9c57e5fdc92bf02
ms.sourcegitcommit: c5e72875206b8c5737c29d5b1ec7b86eec747303
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/17/2018
ms.locfileid: "49382782"
---
# <a name="disable-the-just-in-time-debugger"></a>Wyłączanie debugera Just In Time 

Okno dialogowe debuger just in Time może otworzyć po wystąpieniu błędu w uruchomionej aplikacji i uniemożliwić aplikacji, aby kontynuować. 

Debuger just in Time daje możliwość uruchamiania programu Visual Studio do debugowania błędu. Konieczne jest posiadanie [programu Visual Studio](http://visualstudio.microsoft.com) lub inny wybrany debuger zainstalowana tak, aby wyświetlić szczegółowe informacje o błędzie lub spróbuj go debugować. 

Jeśli jesteś użytkownikiem programu Visual Studio i chcesz wypróbować program do debugowania błędu, zobacz [debugowania za pomocą debugera just in Time](../debugger/debug-using-the-just-in-time-debugger.md). Nie można naprawić ten błąd, czy chcesz zachować debuger just in Time przed otwarciem, możesz [wyłączyć Just-In-Time, debugowanie w programie Visual Studio](debug-using-the-just-in-time-debugger.md#BKMK_Enabling). 

Jeśli masz zainstalowany program Visual Studio, ale nie jest już czy może być konieczne [wyłączyć Just-In-Time, debugowanie z rejestru Windows](debug-using-the-just-in-time-debugger.md#disable-just-in-time-debugging-from-the-windows-registry). 

Jeśli nie masz zainstalowanego programu Visual Studio, można zapobiec debugowanie przez wyłączenie skryptu debugowania lub debugowania po stronie serwera Just In Time. 

- Jeśli próbujesz uruchomić aplikację sieci web, Wyłącz debugowanie skryptu:
  
  W Windows **Panelu sterowania** > **sieć i Internet** > **Opcje internetowe**, wybierz opcję **Wyłącz skryptu (debugowania Internet Explorer)** i **Wyłącz debugowanie skryptu (inne)**. Ustawienia i konkretne kroki zależą od używanej wersji systemu Windows i przeglądarki.
  
  ![Opcje internetowe JIT](../debugger/media/jitinternetoptions.png "Opcje internetowe JIT")
  
- Jeśli hostujesz aplikację sieci web ASP.NET w usługach IIS, należy wyłączyć debugowanie po stronie serwera:

  1. W Menedżerze usług IIS **widoku funkcji**w obszarze **ASP.NET** sekcji, kliknij dwukrotnie **kompilacja platformy .NET**, lub wybierz ją, a następnie wybierz **Otwórz funkcję**w **akcje** okienka. 
  1. W obszarze **zachowanie** > **debugowania**, wybierz opcję **False**. Kroki różnią się w starszych wersjach usług IIS.

Po wyłączeniu debugowania Just-In-Time aplikacji można obsłużyć błąd i będą działać normalnie. 

Jeśli aplikacja ma nadal nieobsługiwany błąd, może zostać wyświetlony komunikat o błędzie lub aplikacja może ulec awarii lub zawieszeniu. Aplikacja nie będzie działać normalnie do czasu naprawienia błędu. Możesz spróbować skontaktować się z właścicielem aplikacji i poproś go, aby rozwiązać ten problem.

