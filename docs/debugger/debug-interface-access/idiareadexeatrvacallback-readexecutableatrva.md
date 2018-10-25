---
title: Idiareadexeatrvacallback::readexecutableatrva — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaReadExeAtRVACallback::ReadExecutableAtRVA method
ms.assetid: 3c1e965f-8f05-41a8-86d8-01830b2377c9
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 69afacf68c77dcb2bca7c951dbd2a1ee9a344cfb
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49917291"
---
# <a name="idiareadexeatrvacallbackreadexecutableatrva"></a>IDiaReadExeAtRVACallback::ReadExecutableAtRVA
Odczytuje określoną liczbę bajtów, zaczynając od określonego względny adres wirtualny (RVA) z pliku wykonywalnego.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT ReadExecutableAtRVA (   
   DWORD  relativeVirtualAddress,  
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `relativeVirtualAddress`  
 [in] RVA w pliku wykonywalnym ma rozpocząć się odczyt.  
  
 `cbData`  
 [in] Liczba bajtów do odczytania.  
  
 `pcbData`  
 [out] Zwraca liczbę odczytanych bajtów.  
  
 `data[]`  
 [out w] Tablica, która jest wypełniane bajtów odczytanych z pliku.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest wywoływana przez kod pomocy technicznej DIA załadować bajtów danych z pliku wykonywalnego przy użyciu względny adres wirtualny. Ta metoda jest wywoływana wspierających [idiadatasource::loaddataforexe —](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiareadexeatrvacallback —](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)   
 [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)