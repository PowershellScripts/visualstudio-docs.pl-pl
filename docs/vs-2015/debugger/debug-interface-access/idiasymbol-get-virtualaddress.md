---
title: Idiasymbol::get_virtualaddress — | Dokumentacja firmy Microsoft
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
- IDiaSymbol::get_virtualAddress method
ms.assetid: dc20c7c0-15a6-4b78-a5c9-2e0b94cac522
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 393d3c57029dc43cb8038bd3452af32834d1046a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49304790"
---
# <a name="idiasymbolgetvirtualaddress"></a>IDiaSymbol::get_virtualAddress
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera adres wirtualny (oceny luk w zabezpieczeniach) lokalizacji. Zastosowania [locationtype — wyliczenie](../../debugger/debug-interface-access/locationtype.md) ustawiono `LocIsStatic`.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT get_virtualAddress (   
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Zwraca adres wirtualny lokalizacji.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` albo kod błędu.  
  
> [!NOTE]
>  Zwracana wartość wynosząca `S_FALSE` oznacza, że właściwość nie jest dostępna dla symbolu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)   
 [LocationType, wyliczenie](../../debugger/debug-interface-access/locationtype.md)



