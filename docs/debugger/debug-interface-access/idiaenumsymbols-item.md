---
title: IDiaEnumSymbols::Item | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumSymbols::Item method
ms.assetid: 2bd1ec04-e677-4e32-8e32-33334f1eed77
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 738b4b5b2e73a55489cc98e6f9e2218568984c68
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumsymbolsitem"></a>IDiaEnumSymbols::Item
Pobiera symbol za pomocą indeksu.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT Item (   
   DWORD        index,  
   IDiaSymbol** symbol  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 indeks  
 [in] Indeks o [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiektu do pobrania. Indeks znajduje się w zakresie od 0 do `count`-1, gdy `count` zwróconego przez [IDiaEnumSymbols::get_Count](../../debugger/debug-interface-access/idiaenumsymbols-get-count.md) metody.  
  
 — symbol  
 [out] Zwraca [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiekt reprezentujący żądany symbol.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumsymbols —](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)