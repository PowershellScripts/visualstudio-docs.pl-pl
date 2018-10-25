---
title: Idiaenumsymbols::Item — | Dokumentacja firmy Microsoft
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
- IDiaEnumSymbols::Item method
ms.assetid: 2bd1ec04-e677-4e32-8e32-33334f1eed77
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a21226f111b646e9197009ce6354095eda64108b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49825658"
---
# <a name="idiaenumsymbolsitem"></a>IDiaEnumSymbols::Item
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera symbol za pomocą indeksu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT Item (   
   DWORD        index,  
   IDiaSymbol** symbol  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 indeks  
 [in] Indeks elementu [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiektu do pobrania. Indeks znajduje się w zakresie od 0 do `count`-1, gdzie `count` jest zwracany przez [idiaenumsymbols::get_count —](../../debugger/debug-interface-access/idiaenumsymbols-get-count.md) metody.  
  
 — symbol  
 [out] Zwraca [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiekt reprezentujący symbol żądaną.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumsymbols —](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



