---
title: "Debugbreak — i __debugbreak | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: DebugBreak
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], DebugBreak function
- DebugBreak function
- breakpoints, DebugBreak function
ms.assetid: 9787c795-df94-4f48-bc8d-3bf899b67421
caps.latest.revision: "23"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1763c117ce9cdb815f12213830079136169b2c35
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="debugbreak-and-debugbreak"></a>DebugBreak i __debugbreak
Można wywołać funkcję debugbreak — Win32 lub [__debugbreak](/cpp/intrinsics/debugbreak) wewnętrzne w dowolnym momencie w kodzie. `DebugBreak`i `__debugbreak` mają ten sam efekt co ustawienie punkt przerwania w tej lokalizacji.  
  
 Ponieważ `DebugBreak` jest wywołanie funkcji systemu, musi być zainstalowany symbole zapewniające informacje stosu wywołań poprawne jest wyświetlany po podziału debugowania systemu. W przeciwnym razie informacje stosu wywołań, wyświetlane przez debuger może być wyłączone przez jedną ramkę. Jeśli używasz `__debugbreak`, symbole nie są wymagane.  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje wewnętrzne kompilatora](/cpp/intrinsics/compiler-intrinsics)   
 [Zabezpieczenia debugera](../debugger/debugger-security.md)   
 [Debugowanie kodu natywnego](../debugger/debugging-native-code.md)   
 [Określ symboli (.pdb) i pliki źródłowe](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)