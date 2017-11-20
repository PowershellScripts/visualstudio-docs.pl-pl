---
title: "Debugowanie w trybie mieszanym jest obsługiwane tylko podczas korzystania z programu Microsoft .NET Framework w wersji 2.0 lub 3.0 | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.error.interop_unsupported_to_old
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: f607af6f-57fe-472a-a32e-b6202067aa96
caps.latest.revision: "5"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dd022d8f0a0e38ffbd7402c69f622df74e24bc30
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="mixed-mode-debugging-is-only-supported-when-using-microsoft-net-framework-20-or-30"></a>Debugowanie w trybie mieszanym jest obsługiwane tylko w przypadku korzystania z programu Microsoft .NET Framework 2.0 or 3.0
Wersje programu Microsoft .NET Framework starszych niż 2.0 nie są dostępne aktualizacje dla debugowanie w trybie mieszanym dla procesów 64-bitowych. Oznacza to, że użytkownik nie można wykonać kroku z kodu zarządzanego do kodu natywnego lub kodu natywnego do zarządzanego kodu podczas debugowania.  
  
 Aby obejść ten problem, można:  
  
-   Aktualizowanie projektu można użyć programu Microsoft .NET Framework 2.0 lub 3.0.  
  
-   Debugowanie kodu zarządzanego i natywnego w oddzielnych sesji debugowania.  
  
-   Debugowanie kodu mieszanych jako proces 32-bitowy, zgodnie z opisem w poniższych procedurach.  
  
### <a name="to-change-the-operating-system-to-32-bit-visual-basic-or-c"></a>Aby zmienić system operacyjny do 32-bitowej (Visual Basic lub C#)  
  
1.  W **Eksploratora rozwiązań**, kliknij prawym przyciskiem myszy projekt, a następnie kliknij przycisk **właściwości** w menu skrótów.  
  
2.  Na stronach właściwości, kliknij przycisk **skompilować** lub **debugowania** kartę.  
  
3.  Kliknij przycisk **platformy**, a następnie wybierz **x86** na liście platform.  
  
     Domyślnie Kompilatory języka Visual Basic i C# generuje kod, aby uruchomić na dowolnym Procesora. Na komputerze 64-bitowym tych plików binarnych Uruchom jako procesów 64-bitowych. Aby uruchomić proces 32-bitowy, musisz wybrać **Win32**, a nie **AnyCPU**.  
  
### <a name="to-change-the-operating-system-to-32-bit-cc"></a>Aby zmienić system operacyjny na 32-bitowych (C/C++)  
  
1.  W **Eksploratora rozwiązań**, kliknij prawym przyciskiem myszy projekt, a następnie kliknij przycisk **właściwości** w menu skrótów.  
  
     Na stronach właściwości, kliknij przycisk **platformy**, a następnie wybierz **Win32** na liście platform.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Zobacz [Konfigurowanie debugowania SQL](http://msdn.microsoft.com/en-us/3db09e68-edcc-42de-9c22-4e97cfd55ab3).  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie aplikacji 64-bitowych](../debugger/debug-64-bit-applications.md)