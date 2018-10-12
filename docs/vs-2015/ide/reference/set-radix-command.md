---
title: Ustaw radix — polecenie | Dokumentacja firmy Microsoft
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
- debug.setradix
helpviewer_keywords:
- Set Radix command
- Debug.SetRadix command
ms.assetid: 6ffd1554-7530-4da4-b5f5-e276a5034f3b
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f0df00cf4c1d1264692be5ab5313eb9f03920b3c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296130"
---
# <a name="set-radix-command"></a>Ustaw Radix — Polecenie
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Ustawia lub zwraca base numeryczne, używany do wyświetlania wartości całkowitych.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.SetRadix [10 | 16 | hex | dec]  
```  
  
## <a name="arguments"></a>Argumenty  
 `10` lub `16` lub `hex` lub `dec`  
 Opcjonalna. Wskazuje dziesiętne (10 lub gru) lub liczba szesnastkowa (16 lub szesnastkowych). Jeśli argument jest pominięty, zwracany jest bieżąca wartość podstawy.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie środowiska, aby wyświetlić wartości całkowite w formacie szesnastkowym.  
  
```  
>Debug.SetRadix hex  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Znajdź/Command — pole](../../ide/find-command-box.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



