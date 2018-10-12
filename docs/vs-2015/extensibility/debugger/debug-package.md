---
title: Pakiet debugowania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], packages
ms.assetid: 99947fd4-fb87-4c69-b26c-65634e17d285
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 61df51b422660a5ea116f136b0d5183e59293a02
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49286328"
---
# <a name="debug-package"></a>Pakiet debugowania
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pakiet debugowania jest uruchamiane w powłoce programu Visual Studio i obsługuje cały interfejs użytkownika. On wykorzystuje interfejsy debugowania programu Visual Studio i komunikuje się z usługą Menedżer debugowania sesji (SDM).  
  
 Zdarzenia przerwania wysyłane za pośrednictwem SDM Przełącz debugera w trybie uruchamiania tryb przerwania i zmianie fokusu do programu, w którym wystąpiło przerwanie. Debugowanie pakietu śledzi ramki stosu i wątku z informacje wysyłane do niej przez zdarzenia.  
  
 Debugowanie pakietu nie ma języka lub zależności środowiska uruchomieniowego. Nie jest niezbędne do wdrożenia lub zmodyfikować pakiet debugowania.  
  
 Debugowanie pakietu jest implementowany przez vsdebug.dll.  
  
## <a name="see-also"></a>Zobacz też  
 [Menedżer debugowania sesji](../../extensibility/debugger/session-debug-manager.md)   
 [Ramki stosu](../../extensibility/debugger/stack-frames.md)   
 [Wątki](../../extensibility/debugger/threads.md)   
 [Składniki debugera](../../extensibility/debugger/debugger-components.md)

