---
title: Instrukcje stop w Visual Basic | Dokumentacja firmy Microsoft
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
helpviewer_keywords:
- End statements
- breakpoints, Stop statements
- debugging managed code, Stop statements vs breakpoints
- Stop statements, about Stop statements
- debugging [Visual Basic], Stop statements vs. breakpoints
ms.assetid: 4ad3fe5c-3dfb-4913-b2eb-a0b635751c18
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f6654489f7b17e3a186b7f2952c7e89067b9e4f7
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="stop-statements-in-visual-basic"></a>Instrukcje stop w Visual Basic
Instrukcji Stop Visual Basic zapewnia programowy alternatywne ustawienia punktu przerwania. Gdy debuger napotka instrukcję Stop, przerywa wykonywanie programu (przejdzie do trybu przerwania). C# programistów można osiągnąć ten sam efekt za pomocą wywołania System.Diagnostics.Debugger.Break.  
  
 Ustawić lub usunąć instrukcję Stop, edytując kod źródłowy. Nie można ustawić lub wyczyścić instrukcje Stop za pomocą poleceń debugera, jak w przypadku punktu przerwania.  
  
 W przeciwieństwie do instrukcji End instrukcji Stop nie Resetuj zmienne lub powrót do trybu projektowania. Można kontynuować z menu debugowanie, aby kontynuować uruchamianie aplikacji.  
  
 Debugowanie jest włączone po uruchomieniu aplikacji Visual Basic poza debugerem instrukcję Stop uruchomi debugera, jeśli Just in Time. Jeśli Just in Time debugowanie nie jest włączone, instrukcja Stop zachowuje się tak, jakby była instrukcji End Kończenie wykonywania. Nie QueryUnload lub Unload zdarzenie, więc musisz usunąć wszystkie instrukcje Stop w wersji aplikacji Visual Basic. Aby uzyskać więcej informacji, zobacz [debugowanie just in Time](../debugger/just-in-time-debugging-in-visual-studio.md).  
  
 Aby uniknąć usunięcia instrukcje Stop, można użyć kompilacja warunkowa:  
  
```  
#If DEBUG Then  
   Stop  
#Else  
   ' Don't stop  
#End If  
```  
  
 Alternatywą jest instrukcja Assert zamiast instrukcji Stop. Instrukcja Debug.Assert dzieli wykonanie tylko wtedy, gdy określony warunek nie jest spełniony, a zostanie automatycznie usunięta, podczas tworzenia wersji. Aby uzyskać więcej informacji, zobacz [potwierdzenia w kod zarządzany](../debugger/assertions-in-managed-code.md). Chcąc instrukcję Assert, która zawsze spowoduje przerwanie wykonywania w wersji do debugowania, możesz to zrobić:  
  
```  
Debug.Assert(false)  
```  
  
 Jeszcze inną alternatywą jest przy użyciu metody Debug.Fail:  
  
```  
Debug.Fail("a clever output string goes here")  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Zabezpieczenia debugera](../debugger/debugger-security.md)   
 [C#, F # i typy projektów Visual Basic](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [Debugowanie zarządzanego kodu](../debugger/debugging-managed-code.md)