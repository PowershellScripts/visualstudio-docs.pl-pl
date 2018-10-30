---
title: 'Porady: debugowanie źródła .NET Framework | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 02/23/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- debugging, .NET Framework source
ms.assetid: fc12e472-ac6a-4e77-8e22-a769e13a03b8
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: c06a2328987201198bc2d5d15a4788d2a821d7b6
ms.sourcegitcommit: d462dd10746624ad139f1db04edd501e7737d51e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/29/2018
ms.locfileid: "50219123"
---
# <a name="how-to-debug-net-framework-source"></a>Porady: debugowanie źródła .NET Framework
Debugowanie źródła .NET Framework, musi mieć dostęp do symboli debugowania dla kodu. Należy również umożliwić stepping do źródła .NET Framework.  
  
 .NET Framework można włączyć przechodzenie krok po kroku i ściąganie symbolu w **opcje** okno dialogowe. Po włączeniu pobierania symboli, można od razu pobrać symbole lub po prostu włączyć opcję późniejszego pobrania. Jeśli użytkownik nie pobierze symboli natychmiast, symbole będą pobierane przy następnym uruchomieniu debugowania aplikacji. Możesz także zrobić ręczne pobranie z **modułów** okna lub **stos wywołań** okna.  
  
### <a name="to-enable-net-framework-source-debugging"></a>Aby włączyć debugowanie źródła .NET Framework  
  
1.  Na **narzędzia** menu, kliknij przycisk **opcje**.  
  
2.  W **opcje** okno dialogowe, kliknij przycisk **debugowanie** kategorii.  
  
3.  W **ogólne** polu **źródła Włącz .NET Framework przechodzenie krok po kroku.**  
  
    1.  Jeśli masz włączoną opcję tylko mój kod, okno dialogowe ostrzeżenia informuje, że tylko mój kod jest teraz wyłączony. Kliknij przycisk **OK**.  
  
    2.  Jeśli nie masz ustawione lokalizacji pamięci podręcznej symboli, osobne okno dialogowe ostrzeżenia informuje, że teraz ustawiono domyślną lokalizacji pamięci podręcznej symboli. Kliknij przycisk **OK**.  
  
4.  W obszarze **debugowanie** kategorię, kliknij przycisk **symbole**.  
  
5.  Jeśli chcesz zmienić lokalizację pamięci podręcznej symboli, Edytuj lokalizację w **pamięci podręcznej symboli w tym katalogu** lub kliknij przycisk **Przeglądaj** aby wybrać lokalizację.  
  
6.  Jeśli chcesz pobrać symbole natychmiast, kliknij przycisk **Załaduj symbole z powyższych lokalizacji**.  
  
     Ten przycisk nie jest dostępna w trybie projektowania, ale jest dostępne podczas debugowania.  
  
     Jeśli użytkownik nie chce pobrać symboli teraz, symbole będą pobierane automatycznie przy następnym uruchomieniu debugowania programu.  
  
7.  Kliknij przycisk **OK** zamknąć **opcje** okno dialogowe.  
  
### <a name="to-load-framework-symbols-using-the-modules-window"></a>Aby załadować symbole Framework w oknie modułów  
  
1.  W **modułów** okna (podczas debugowania, wybierz **debugowania** > **Windows** > **modułów**), Kliknij prawym przyciskiem myszy moduł, dla której symbole nie są ładowane. Można stwierdzić, czy symbole są załadowane lub nie, patrząc **stan symboli** kolumny.  
  
2.  Wskaż **ustawienia symboli** i kliknij przycisk **serwery symboli firmy Microsoft** można pobrać symbole z serwera publicznego symboli firmy Microsoft. Alternatywnie możesz kliknąć prawym przyciskiem myszy moduł i wybrać **załadować symbole** załadować z katalogu, w którym symbole zostały wcześniej zapisane.  
  
### <a name="to-load-framework-symbols-using-the-call-stack-window"></a>Aby załadować symbole Framework w oknie stosu wywołań  
  
1.  W **stos wywołań** okna, kliknij prawym przyciskiem myszy ramkę, dla której symbole nie są ładowane. Ramki będą wyszarzone.  
  
2.  Wskaż **ustawienia symboli** i kliknij przycisk **serwery symboli firmy Microsoft**, lub kliknij prawym przyciskiem myszy moduł i wybierz pozycję **ścieżki symboli**.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie zarządzanego kodu](../debugger/debugging-managed-code.md)   
 [Określanie plików symboli (pdb) i plików źródłowych](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)