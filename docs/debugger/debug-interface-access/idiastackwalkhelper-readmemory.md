---
title: IDiaStackWalkHelper::readMemory | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaStackWalkHelper2::readMemory method
ms.assetid: e1eb90aa-49b7-476c-9e70-7e8f08994cbe
caps.latest.revision: "11"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: cccec7df8428db0a1e7c1fe2274475c2b723d760
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiastackwalkhelperreadmemory"></a>IDiaStackWalkHelper::readMemory
Odczytuje blok danych z obrazu wykonywalnego w pamięci.  
  
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
 [in] Wartość z zakresu od [memorytypeenum — wyliczenie](../../debugger/debug-interface-access/memorytypeenum.md) wyliczenie opisujące typ pamięci odczytać.  
  
 Va  
 [in] Wirtualny adres w obrazie, w którym ma rozpocząć się odczyt.  
  
 `cbData`  
 [in] Rozmiar buforu danych w bajtach.  
  
 `pcbData`  
 [out] Zwraca liczbę bajtów odczytanych w rzeczywistości. Jeśli `pbData` jest `NULL`, a następnie jest to całkowita liczba bajtów danych dostępne.  
  
 `pbData`  
 [w, out] Buforu, który jest wypełniane pamięci odczytać.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [Memorytypeenum — wyliczenie](../../debugger/debug-interface-access/memorytypeenum.md)