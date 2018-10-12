---
title: Ustaw bieżący proces | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Debug.SetCurrentProcess command
- Set Current Process command
ms.assetid: 1e016ebd-aadd-411f-a606-03bf69d3f8aa
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 0baea39c341e8034ff222de32548d0518f115e82
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49246665"
---
# <a name="set-current-process"></a>Ustaw bieżący proces
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Ustawia określony proces jako aktywny procesu w debugerze.  
  
## <a name="syntax"></a>Składnia  
  
```  
Debug.SetCurrentProcess index  
```  
  
## <a name="arguments"></a>Argumenty  
 `index`  
 Wymagane. Indeks procesu.  
  
## <a name="remarks"></a>Uwagi  
 Podczas debugowania, ale tylko jeden proces jest aktywny w programie do usuwania błędów w dowolnym momencie można dołączyć do wielu procesów. Możesz użyć `SetCurrentProcess` polecenie, aby ustawić aktywny proces.  
  
## <a name="example"></a>Przykład  
  
```  
>Debug.SetCurrentProcess 1  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Visual Studio — polecenia](../../ide/reference/visual-studio-commands.md)   
 [Okno polecenia](../../ide/reference/command-window.md)   
 [Visual Studio — aliasy poleceń](../../ide/reference/visual-studio-command-aliases.md)



