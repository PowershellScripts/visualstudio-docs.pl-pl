---
title: IDiaEnumLineNumbers::Next | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumLineNumbers::Next method
ms.assetid: 363d5b40-1316-4ab8-836f-63637f619e0a
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 627a6e2dd0e319cbcdccfa5824d9c379faa0d049
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumlinenumbersnext"></a>IDiaEnumLineNumbers::Next
Pobiera określoną liczbę numerów wierszy w kolejności wyliczenia.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT Next (   
   ULONG            celt,  
   IDiaLineNumber** rgelt,  
   ULONG*           pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 celt  
 [in] Liczba numerów wierszy w moduł wyliczający, które mają zostać pobrane.  
  
 rgelt  
 [out] Zwraca tablicę [idialinenumber —](../../debugger/debug-interface-access/idialinenumber.md) obiekty reprezentujące żądane numery.  
  
 pceltFetched  
 [out] Zwraca liczbę numerów wierszy w pobranych modułu wyliczającego.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`. Zwraca `S_FALSE` przypadku bez więcej numerów wierszy. W przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumlinenumbers —](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [Idialinenumber —](../../debugger/debug-interface-access/idialinenumber.md)   
 [IDiaSession::findLinesByLinenum](../../debugger/debug-interface-access/idiasession-findlinesbylinenum.md)