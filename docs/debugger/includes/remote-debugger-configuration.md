---
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.openlocfilehash: 252c505260986bd08b5522ba79d1e00a82624241
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942962"
---
Musi mieć uprawnienia administracyjne na komputerze zdalnym.  
  
1. Znajdź aplikację zdalny debuger. (Znajdź msvsmon.exe w lokalizacji, w których została zainstalowana lub Otwórz Start menu i poszukaj **zdalny debuger**.)
  
    Jeśli używasz zdalnego debugera na serwerze zdalnym, możesz kliknij prawym przyciskiem myszy aplikację zdalny debuger i wybrać **Uruchom jako administrator**. Jeśli nie używasz go na serwerze zdalnym, wystarczy ją uruchomić normalnie.
  
2. Po uruchomieniu narzędzia zdalne po raz pierwszy (lub przed jej skonfigurowano), **Konfiguracja zdalnego debugowania** pojawi się okno dialogowe.  
  
    ![RemoteDebuggerConfWizardPage](../media/remotedebuggerconfwizardpage.png "RemoteDebuggerConfWizardPage")  
  
3. Jeśli interfejs API usługi Windows nie jest zainstalowany (co się stanie, tylko w systemie Windows Server 2008 R2), wybierz opcję **zainstalować** przycisku.  
  
4. Wybierz typy sieci, należy użyć narzędzi zdalnych na. Należy wybrać co najmniej jeden typ sieci. Jeśli komputery są połączone za pośrednictwem domeny, należy wybrać pierwszy element. Jeśli komputery są połączone za pośrednictwem grupy roboczej lub grupa domowa, musisz wybrać drugi lub trzeci element zgodnie z potrzebami.  
  
5. Wybierz **Konfiguruj zdalne debugowanie** Aby skonfigurować zaporę i uruchomić narzędzie.  
  
6. Po zakończeniu konfiguracji zostanie wyświetlone okno zdalnego debugera.
  
    ![RemoteDebuggerWindow](../media/remotedebuggerwindow.png "RemoteDebuggerWindow")
  
    Zdalny debuger jest teraz oczekiwania na połączenie. Zanotuj nazwę serwera i port numer, który jest wyświetlany, ponieważ musi on być zgodny konfiguracji używanej później w programie Visual Studio.  
  
   Po zakończeniu debugowania i musisz zatrzymać debuger zdalny kliknij **Plik > Zakończ** w oknie. Możesz ponownie uruchomić go z **Start** menu lub z wiersza polecenia:  
  
   **\<Debuger zdalny katalog instalacyjny >\\< x86, x64, ARM, ARM64 lub Appx > \msvsmon.exe**.  
