---
title: IDiaStackWalkHelper::readMemory | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2::readMemory method
ms.assetid: e1eb90aa-49b7-476c-9e70-7e8f08994cbe
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 76b054d004e6c62f9d36ca5fcebe1a7f0476fbfc
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49825860"
---
# <a name="idiastackwalkhelperreadmemory"></a>IDiaStackWalkHelper::readMemory
Odczytuje blok danych z pliku wykonywalnego obrazu w pamięci.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT readMemory(   
   enum MemoryTypeEnum type,  
   ULONGLONG           va,  
   DWORD               cbData,  
   DWORD*              pcbData,  
   BYTE*               pbData  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `type`  
 [in] Wartość z zakresu od [memorytypeenum — wyliczenie](../../debugger/debug-interface-access/memorytypeenum.md) wyliczenie opisujące typ pamięci do odczytu.  
  
 oceny luk w zabezpieczeniach  
 [in] Wirtualny adres obrazu, w którym ma rozpocząć się odczyt.  
  
 `cbData`  
 [in] Rozmiar buforu danych w bajtach.  
  
 `pcbData`  
 [out] Zwraca liczbę bajtów odczytanych w rzeczywistości. Jeśli `pbData` jest `NULL`, a następnie jest to całkowita liczba bajtów dostępnych danych.  
  
 `pbData`  
 [out w] Buforu, który jest wypełniane pamięci odczytu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [MemoryTypeEnum, wyliczenie](../../debugger/debug-interface-access/memorytypeenum.md)