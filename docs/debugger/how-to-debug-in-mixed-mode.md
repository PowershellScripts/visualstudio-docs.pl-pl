---
title: 'Porady: debugowanie w trybie mieszanym | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 06/19/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging DLLs
- debugging [Visual Studio], mixed-mode
- mixed-mode debugging
ms.assetid: 2859067d-7fcc-46b0-a4df-8c2101500977
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8a08cf3cf95073d06c1dfa350f2de86bf72837c5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49182679"
---
# <a name="how-to-debug-in-mixed-mode"></a>Porady: debugowanie w trybie mieszanym
W poniższych procedurach opisano sposób włączania debugowania dla kodu zarządzanego i natywnego razem, znany także jako trybu mieszanego debugowania. Istnieją dwa scenariusze debugowania w trybie mieszanym:  
  
- Aplikacji, która wywołuje bibliotekę DLL są zapisywane w kodzie natywnym, a Biblioteka DLL jest zarządzana. 
  
- Aplikacja, która wywołuje bibliotekę DLL są zapisywane w kodzie zarządzanym i Wspomniany plik znajduje się w kodzie natywnym. Aby uzyskać samouczek, który przeprowadzi Cię przez ten scenariusz bardziej szczegółowo, zobacz [debugowanie kodu zarządzanego i natywnego](../debugger/how-to-debug-managed-and-native-code.md).
   
Możesz włączyć debugery zarządzane i natywne w projekcie aplikacji wywołującej **właściwość** stron. Ustawienia różnią się natywnych i zarządzanych aplikacji. 

Jeśli nie masz dostępu do projektu wywołującej aplikacji można debugować bibliotekę DLL z projektu DLL. Tryb mieszany, aby debugować tylko projekt DLL nie jest konieczne. Aby uzyskać więcej informacji, zobacz [porady: debugowanie z projektu DLL](../debugger/how-to-debug-from-a-dll-project.md). 

> [!NOTE]
> Dostępne polecenia i okien dialogowych mogą różnić się od przedstawionych w tym artykule, w zależności od wersji lub ustawienia programu Visual Studio. Aby zmienić swoje ustawienia, wybierz opcję **narzędzia** > **Import i eksport ustawień**. Aby uzyskać więcej informacji, zobacz [personalizowanie środowiska IDE programu Visual Studio](../ide/personalizing-the-visual-studio-ide.md).

## <a name="enable-mixed-mode-debugging-for-a-native-calling-app"></a>Włącz debugowanie w trybie mieszanym dla natywnych aplikacji wywołującej  
  
1. Wybierz projekt C++ w **Eksploratora rozwiązań** i kliknij przycisk **właściwości** ikonę, naciśnij klawisz **Alt**+**Enter**, lub Kliknij prawym przyciskiem myszy i wybierz polecenie **właściwości**.
   
1. W  **\<Projekt > strony właściwości** okna dialogowego rozwiń **właściwości konfiguracji**, a następnie wybierz pozycję **debugowanie**.  
   
1. Ustaw **typ debugera** do **mieszane** lub **automatycznie**.
   
1. Wybierz **OK**.
   
   ![Włącz debugowanie w trybie mieszanym](../debugger/media/dbg-mixed-mode-from-native.png "włączyć debugowanie w trybie mieszanym")

## <a name="enable-mixed-mode-debugging-for-a-managed-calling-app"></a>Włącz debugowanie w trybie mieszanym dla zarządzanych aplikacji wywołującej  
  
1. Wybierz projekt C# lub Visual Basic w **Eksploratora rozwiązań** i wybierz **właściwości** ikonę, naciśnij klawisz **Alt**+**Enter**, lub kliknij prawym przyciskiem myszy i wybierz pozycję **właściwości**.
   
1. Wybierz **debugowania** , a następnie wybierz pozycję **Włącz debugowanie kodu natywnego**.
   
1. Użyj **pliku** > **Zapisz wybrane elementy** lub **Ctrl + S** można zapisać zmian.

   ![Włącz debugowanie kodu natywnego](../debugger/media/dbg-mixed-mode-from-csharp.png "Włącz debugowanie kodu natywnego")
  
## <a name="see-also"></a>Zobacz także  
 [Instrukcje: debugowanie z projektu DLL](../debugger/how-to-debug-from-a-dll-project.md)