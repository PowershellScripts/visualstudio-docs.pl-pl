---
title: 'Debugowanie F # | Dokumentacja firmy Microsoft'
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
- Debugging [F#]
- F#, debugging
ms.assetid: 20bcd51c-2d06-4281-9a1e-ef2b91d1a779
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dd722e40a0579181e3c361706f0775aaf350c341
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49209576"
---
# <a name="debugging-f"></a>Debugowanie F# #
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Debugowanie F # jest podobne do debugowania jakiegokolwiek języka zarządzanego, z pewnymi wyjątkami:  
  
-   **Autos** okna nie są wyświetlane zmienne F #.  
  
-   Edytuj i Kontynuuj nie jest obsługiwane w języku F #. Edytowanie kodu F # podczas sesji debugowania jest możliwe, ale należy unikać. Ponieważ zmiany w kodzie nie są stosowane podczas sesji debugowania, edytowanie F # kodu podczas debugowania spowoduje niezgodność między kodem źródłowym i debugowany kod.  
  
-   Debuger nie może rozpoznać wyrażeń języka F #. Aby wprowadzić wyrażenie w oknie debugera lub okno dialogowe podczas debugowania F #, wykonuje translację wyrażenia w języku C# składni. Podczas tłumaczenia jest wyrażenie F # do języka C#, upewnij się, że należy pamiętać, że C# używa == jako operator porównania dla równości i że F # używa pojedynczego =.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie kodu zarządzanego](../debugger/debugging-managed-code.md)



