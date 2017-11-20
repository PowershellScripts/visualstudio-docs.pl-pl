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
ms.openlocfilehash: a55b2a12c9a45c5a3952e3e6f4e1627bec8ba520
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
1. W **Eksploratora rozwiązań**, kliknij prawym przyciskiem myszy węzeł projektu i wybierz **publikowania** (formularzy sieci Web **publikowania aplikacji sieci Web**).

2. W **publikowania** okno dialogowe, wybierz opcję **folderu**, kliknij przycisk **Przeglądaj**i Utwórz nowy folder **C:\Publish**.

    ![RemoteDBG_Publish_Local](../media/remotedbg_publish_local.png "RemoteDBG_Publish_Local")

    W przypadku aplikacji formularzy sieci Web wybierz **niestandardowy** w oknie dialogowym Publikowanie, wprowadź nazwę profilu, a następnie wybierz pozycję **OK**.

3. Kliknij przycisk **publikowania**.

    Visual Studio publikuje projektu do folderu. Przedstawia postęp w oknie danych wyjściowych.

4. W **publikowania** okno dialogowe, kliknij przycisk **ustawienia** łącza, a następnie wybierz **ustawienia** kartę.

5. Ustaw dla konfiguracji **debugowania**, wybierz pozycję **Usuń wszystkie istniejące pliki przez opublikowaniem**, a następnie kliknij przycisk **zapisać**.

    > [!NOTE]
    > Jeśli używasz kompilacji wydania wyłączeniu debugowania w pliku web.config podczas publikowania.

6. Kliknij przycisk **publikowania**.

    ![RemoteDBG_Publish_Debug_Config](../media/remotedbg_publish_debug_config.png "RemoteDBG_Publish_Debug_Config")
    
    Publikowanie aplikacji **debugowania** konfiguracji projektu do folderu lokalnego.

5. Skopiuj katalog projektu ASP.NET z komputera programu Visual Studio do katalogu lokalnego skonfigurowane dla aplikacji ASP.NET (w tym przykładzie **C:\Publish**) na komputerze z systemem Windows Server. W tym samouczku przyjęto założenie, kopiowane są ręcznie, ale można użyć innych narzędzi, takich jak programu PowerShell, Xcopy lub Robocopy.

    > [!CAUTION]
    >  Jeśli chcesz dokonać zmian kodu lub skompiluj ponownie, należy ponownie opublikować i powtórz ten krok. Plik wykonywalny skopiowane na komputer zdalny musi dokładnie odpowiadać lokalnego źródłowe i symboli.

6. W systemie Windows Server Sprawdź, że aplikację można uruchomić poprawnie, otwierając aplikację w przeglądarce.

    Jeśli aplikacja nie działa prawidłowo, może być niezgodność między wersji platformy ASP.NET zainstalowanej na serwerze i komputerze Visual Studio lub może wystąpić problem z konfiguracją usług IIS lub witryny sieci Web. Ponownie sprawdź wcześniejszych krokach.