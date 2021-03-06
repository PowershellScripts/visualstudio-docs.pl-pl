---
title: Idiaenumdebugstreamdata::Item — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreamData::Item method
ms.assetid: 761e61a5-44a6-4d5d-a98e-c2e9b89d2343
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5101c5f43e3d931a0ec4653838e4b45c01d3c5fb
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49936309"
---
# <a name="idiaenumdebugstreamdataitem"></a>IDiaEnumDebugStreamData::Item
Pobiera określony rekord.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT Item (   
   DWORD  index,  
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 indeks  
 [in] Indeks rekordu do pobrania. Indeks znajduje się w zakresie od 0 do `count`-1, gdzie `count` jest zwracany przez [idiaenumdebugstreamdata::get_count —](../../debugger/debug-interface-access/idiaenumdebugstreamdata-get-count.md).  
  
 cbData  
 [in] Rozmiar buforu danych, w bajtach.  
  
 pcbData  
 [out] Zwraca liczbę bajtów zwróconych. Jeśli `data` jest `NULL`, następnie `pcbData` zawiera całkowitą liczbę bajtów danych dostępnych w określonego rekordu.  
  
 dane]  
 [out] Bufor, który jest wypełniane dane rekord strumienia debugowania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwraca `E_INVALIDARG` dla nieprawidłowe parametry i, jeśli `index` parametr jest spoza zakresu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumdebugstreamdata —](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)   
 [Idiaenumdebugstreamdata::Next —](../../debugger/debug-interface-access/idiaenumdebugstreamdata-next.md)   
 [Idiaenumdebugstreams::Item —](../../debugger/debug-interface-access/idiaenumdebugstreams-item.md)   
 [Idiaenumdebugstreamdata::get_count —](../../debugger/debug-interface-access/idiaenumdebugstreamdata-get-count.md)   
 [IDiaEnumDebugStreamData::Skip](../../debugger/debug-interface-access/idiaenumdebugstreamdata-skip.md)