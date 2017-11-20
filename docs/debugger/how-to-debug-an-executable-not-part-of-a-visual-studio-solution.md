---
title: "Porady: debugowanie pliku wykonywalnego, który nie jest częścią rozwiązania Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugging [Visual Studio], executables
- executable files, importing
- executable files, debugging outside of projects
ms.assetid: 3ea176e8-1ce5-42c4-b7a2-abe3a2765033
caps.latest.revision: "23"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: be07be0e1374360a96b6672b095dcc039c6bb4f0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-debug-an-executable-that-is-not-part-of-a-visual-studio-solution"></a>Porady: debugowanie pliku wykonywalnego, który nie jest częścią rozwiązania programu Visual Studio
Czasami może chcesz debugować plik wykonywalny (.exe plik), który nie jest częścią [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] projektu. Może być utworzony poza plik wykonywalny [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] lub pliku wykonywalnego otrzymany od kogoś innego.  
  
Zwykle odpowiedzią na ten problem ma uruchomić plik wykonywalny poza Visual Studio i Dołącz do niej przy użyciu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] debugera. Aby uzyskać więcej informacji, zobacz [dołączyć do uruchamiania procesów](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).  
  
Dołączanie do aplikacji wymaga niektórych ręczne wykonanie czynności, dlatego zajmuje kilka sekund. To niewielkie opóźnienie oznacza, że dołączanie nie pomoże, jeśli chcesz debugować problem występujący podczas uruchamiania. Ponadto jeśli debugowany program, który nie oczekuje danych wejściowych użytkownika i kończy się szybko, nie masz czasu można dołączyć do niego. Jeśli masz [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] i [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] zainstalowana, można utworzyć projektu EXE dla takiego programu.

> [!NOTE]
>  Nie wszystkie języki programowania obsługuje projekty EXE.

Podczas debugowania pliku wykonywalnego, który nie jest częścią rozwiązania Visual Studio, dostępne funkcje debugowania można ograniczyć, czy dołączyć do uruchomienia pliku wykonywalnego lub Dodaj plik wykonywalny do [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] rozwiązania.

- Jeśli masz kod źródłowy, najlepiej zaimportować kodu źródłowego w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] i Utwórz kompilację debugowania pliku wykonywalnego w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].
- Jeśli nie masz kod źródłowy i plik wykonywalny został skompilowany bez [informacje o debugowaniu](../debugger/how-to-set-debug-and-release-configurations.md) w formacie zgodnym z, dostępne funkcje debugowania są bardzo ograniczone. 
  
### <a name="to-create-an-exe-project-for-an-existing-executable"></a>Aby utworzyć plik EXE projektu dla istniejącego pliku wykonywalnego  
  
1.  Na **pliku** menu, kliknij przycisk **Otwórz** i wybierz **projektu**.  
  
2.  W **Otwórz projekt** okno dialogowe, kliknij przycisk Dalej, aby wyświetlić listę listy rozwijanej **nazwę pliku** i wybierz **wszystkie pliki projektu**.  
  
3.  Zlokalizuj plik wykonywalny, a następnie kliknij przycisk **OK**.  

    Spowoduje to utworzenie tymczasowego rozwiązania, które zawiera pliku wykonywalnego.

5.  Uruchom plik wykonywalny, wybierając polecenie wykonywania, takie jak **Start**, z **debugowania** menu.    
  
### <a name="to-import-an-executable-into-a-visual-studio-solution"></a>Aby zaimportować plik wykonywalny do rozwiązania Visual Studio  
  
1.  Na **pliku** menu wskaż **Dodawanie projektu**, a następnie kliknij przycisk **istniejący projekt**.  
  
2.  W **Dodaj istniejący projekt** okno dialogowe, kliknij przycisk Dalej, aby wyświetlić listę listy rozwijanej **nazwę pliku** i wybierz **wszystkie pliki projektu**.  
  
3.  Znajdź i zaznacz plik wykonywalny.  
  
4.  Kliknij przycisk **OK**.  
  
5.  Uruchom plik wykonywalny, wybierając polecenie wykonywania, takie jak **Start**, z **debugowania** menu.    
  
## <a name="see-also"></a>Zobacz też  
 [Ustawienia debugowania i przygotowanie](../debugger/debugger-settings-and-preparation.md)   
 [Zabezpieczenia debugera](../debugger/debugger-security.md)   
 [DBG, pliki](http://msdn.microsoft.com/en-us/91e449e9-8b65-4123-960f-2107cd1f1cfd)