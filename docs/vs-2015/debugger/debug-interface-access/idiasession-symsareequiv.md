---
title: Idiasession::symsareequiv — | Dokumentacja firmy Microsoft
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
- C++
helpviewer_keywords:
- IDiaSession::symsAreEquiv method
ms.assetid: 9941d520-e203-46c0-83c3-b3a967f4fc59
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 936097cf16e8f933cda2289cb0b6131eb0e8a3c2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49266009"
---
# <a name="idiasessionsymsareequiv"></a>IDiaSession::symsAreEquiv
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Sprawdza, czy dwa symbole są równoważne.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT symsAreEquiv (   
   IDiaSymbol* symbolA,  
   IDiaSymbol* symbolB  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `symbolA`  
 [in] Pierwszy [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiekt używany do porównania.  
  
 `symbolB`  
 [in] Drugi `IDiaSymbol` obiekt używany do porównania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Symbole są równoważne, funkcja zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE`, symbole nie są równoważne. W przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



