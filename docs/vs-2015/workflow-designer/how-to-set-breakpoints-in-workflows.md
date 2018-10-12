---
title: 'Porady: Ustawianie punktów przerwania w przepływach pracy | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e41b21c9-c061-4358-8e2f-eb5e412864a8
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 18d87e523e9c0456f0f80add89c2ade32cf903fa
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49199813"
---
# <a name="how-to-set-breakpoints-in-workflows"></a>Porady: Ustawianie punktów przerwania w przepływach pracy
Kiedy używasz [!INCLUDE[wfd1](../includes/wfd1-md.md)], możesz ustawić punkty przerwania na graficzny przepływów pracy, tak jak w kodzie języka Visual Basic lub C#. Zgodnie z oczekiwaniami, zatrzyma wykonywanie przepływu pracy, w każdym punkcie przerwania, który został ustawiony.  
  
 Punkt przerwania ma trzy stany: *oczekujące*, *powiązany*, i *błąd*. Po ustawieniu punktu przerwania jest oczekujące i jest reprezentowana przez stałe czerwoną ikonę. Po załadowaniu szablonu przepływu pracy środowiska uruchomieniowego staje się powiązany. Jeśli określisz ma niewłaściwy format dla punktu przerwania, takich jak nazwa działania, który nie jest prawidłowy, pojawi się okno błędu. Punkt przerwania nadal jest dodawany do okna punkt przerwania, ale jest oznaczony za pomocą małych "x".  
  
> [!NOTE]
>  Ustawianie punktów przerwania w przepływach pracy, wywoływane jest nieobsługiwana.  
  
> [!WARNING]
>  Upewnij się, że wybrano opcję **Włącz tylko mój kod (tylko zarządzany)** z **narzędzia**, **opcje**, **debugowanie** menu przed debugowanie. Jeśli masz dwie sekwencje zagnieżdżone w obrębie innej sekwencji, a następnie ustaw punkt przerwania w pierwszej sekwencji wewnętrzny, naciskając klawisz **F11** nie będzie debugowania do drugiej sekwencji wewnętrzny, jeśli **Włącz tylko mój kod (tylko zarządzany)** nie wybrano opcji.  
  
> [!WARNING]
>  Punkty przerwania w przepływie pracy nie zostanie pobieranie odwołań, jeśli Pełna ścieżka do właściwości pliku XAML nie jest dokładne. Pełna ścieżka do pliku XAML nie jest dokładne po przeniesieniu projektu/rozwiązania do innego folderu lub innego komputera. Wybierz klawisze Ctrl + S, aby zapisać i zaktualizować właściwość pełną ścieżkę.  
  
### <a name="to-set-a-breakpoint-on-an-activity-in-the-design-view"></a>Aby ustawić punkt przerwania w działaniu w widoku projektu  
  
1.  Wybierz czynność chcesz, aby debuger przerywał działanie w przypadku.  
  
2.  Na **debugowania** menu, wybierz opcję **Przełącz punkt przerwania**. Czerwona ikona pojawi się do górnej krawędzi lewej działania.  
  
     Alternatywnie można również nacisnąć skrót **F9** klucza po wybraniu działania lub można kliknij prawym przyciskiem myszy działanie i wybierz opcję **punktu przerwania** następnie **Wstaw punkt przerwania**z menu kontekstowego.  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: wywoływanie debugera przepływu pracy](../workflow-designer/how-to-invoke-the-workflow-debugger.md)   
 [Debugowanie przepływów pracy za pomocą projektanta przepływu pracy](../workflow-designer/debugging-workflows-with-the-workflow-designer.md)   
 [Instrukcje: Debugowanie kodu XAML za pomocą Projektanta przepływu pracy](../workflow-designer/how-to-debug-xaml-with-the-workflow-designer.md)