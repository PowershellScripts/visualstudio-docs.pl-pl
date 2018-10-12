---
title: Przełącz punkt przerwania — polecenie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- debug.togglebreakpoint
helpviewer_keywords:
- ToggleBreakpoint command
- Debug.ToggleBreakPoint command
- Toggle Breakpoint command
ms.assetid: d50dfadb-ce79-4d5e-9c09-1cfddd57876d
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f993d9a0377531b155301bed235c00bf8e6667c4
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223161"
---
# <a name="toggle-breakpoint-command"></a>Przełącz punkt przerwania — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Włącza punkt przerwania lub wyłączyć, w zależności od bieżącego stanu w bieżącej lokalizacji w pliku.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.ToggleBreakpoint [text]  
```  
  
## <a name="arguments"></a>Argumenty  
 `text`  
 Opcjonalna. Jeśli tekst jest określona, wiersz jest oznaczona jako nazwany punkt przerwania. W przeciwnym razie wiersz jest oznaczona jako nienazwane punkt przerwania, który przypomina co się stanie, gdy klawisz F9.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład zmienia bieżący punkt przerwania.  
  
```  
>Debug.ToggleBreakpoint  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



