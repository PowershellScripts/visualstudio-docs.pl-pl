---
title: IDiaInjectedSource::get_source | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaInjectedSource::get_source method
ms.assetid: 3c0b5386-321f-4f8f-85cc-e2ee7b4cc3d2
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 910b96d4114617957907ff1cd4eee4609ebaa250
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiainjectedsourcegetsource"></a>IDiaInjectedSource::get_source
Pobiera bajtów kodu źródłowego.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_source (   
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `cbData`  
 [in] Liczba bajtów reprezentujący rozmiar buforu danych.  
  
 `pcbData`  
 [out] Zwraca liczbę bajtów reprezentujący bajtów zwracana. Jeśli `data` jest `NULL`, następnie `pcbData` jest całkowita liczba bajtów danych jest dostępna.  
  
 `data[]`  
 [out] Buforu, który ma zostać wypełnione bajtów źródła.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`. Zwraca `S_FALSE` Jeśli ta właściwość nie jest obsługiwana. W przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiainjectedsource —](../../debugger/debug-interface-access/idiainjectedsource.md)