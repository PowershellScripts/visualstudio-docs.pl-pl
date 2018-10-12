---
title: 'Porady: debugowanie metody OnStart | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- OnStart method
- debugging [Visual Studio], Windows services
- debugging managed code, OnStart method
- debugging Windows Services applications, OnStart method
- Windows Service applications, debugging
ms.assetid: b06b5d65-424b-490f-bf58-97583cd7006a
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 59f54b407436f9ebdeab3fac275068e843398f36
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49221250"
---
# <a name="how-to-debug-the-onstart-method"></a>Porady: debugowanie metody OnStart
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Usługa Windows można debugować, uruchamiając usługi i dołączanie debugera do procesu usługi. Aby uzyskać więcej informacji, zobacz [porady: debugowanie aplikacji usług Windows](http://msdn.microsoft.com/library/63ab0800-0f05-4f1e-88e6-94c73fd920a2). Jednak aby debugować <xref:System.ServiceProcess.ServiceBase.OnStart%2A?displayProperty=fullName> metody usługi Windows, można uruchomić debugera z wewnątrz metody.  
  
1.  Dodaj wywołanie do <xref:System.Diagnostics.Debugger.Launch%2A> na początku `OnStart()`metody.  
  
    ```csharp  
    protected override void OnStart(string[] args)  
    {  
        System.Diagnostics.Debugger.Launch();  
     }  
    ```  
  
2.  Uruchom usługę (możesz użyć `net start`, lub uruchomić go w **usług** okno).  
  
     Powinny pojawić się okno dialogowe podobne do następującego:  
  
     ![OnStartDebug](../debugger/media/onstartdebug.png "OnStartDebug")  
  
3.  Wybierz **tak, debugowanie \<nazwa usługi >.**  
  
4.  W oknie debugera just in Time wybierz wersję programu Visual Studio, którego chcesz użyć do debugowania.  
  
     ![JustInTimeDebugger](../debugger/media/justintimedebugger.png "JustInTimeDebugger")  
  
5.  Nowe wystąpienie programu Visual Studio uruchomi się i wykonywania jest zatrzymywany w `Debugger.Launch()` metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Zabezpieczenia debugera](../debugger/debugger-security.md)   
 [Debugowanie kodu zarządzanego](../debugger/debugging-managed-code.md)



