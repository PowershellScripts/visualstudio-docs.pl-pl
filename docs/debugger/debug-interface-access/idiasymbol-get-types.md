---
title: IDiaSymbol::get_types | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSymbol::get_types method
ms.assetid: 5f056e0c-e15b-4e00-8f78-aadc8574f7ea
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c53a8866856288aa039c0e23b6244da80184285d
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasymbolgettypes"></a>IDiaSymbol::get_types
Pobiera tablicę typów kompilatora specyficzne dla tego symbolu.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_types (   
   DWORD       cTypes,  
   DWORD*      pcTypes,  
   IDiaSymbol* types[]  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `cTypes`  
 [in] Rozmiar buforu do przechowywania danych.  
  
 `pcTypes`  
 [out] Zwraca liczbę typów zapisywane, lub jeśli `types` parametr jest `NULL`, następnie całkowita liczba dostępnych typów.  
  
 `types[]`  
 [out] Tablica, która ma być wypełnione przy użyciu [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiektów, które reprezentują wszystkie typy dla tego symbolu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` lub kod błędu.  
  
> [!NOTE]
>  Zwracana wartość `S_FALSE` oznacza, że właściwość nie jest dostępna symbolu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)