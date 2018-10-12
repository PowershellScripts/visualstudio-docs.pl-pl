---
title: Idiasectioncontrib::get_code — | Dokumentacja firmy Microsoft
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
- IDiaSectionContrib::get_code method
ms.assetid: f9ccf7a6-46e7-4a1d-9d5c-97272e17bbbb
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7f18fbbf2a3f9269a4073e8802ec13a34090d67a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49201960"
---
# <a name="idiasectioncontribgetcode"></a>IDiaSectionContrib::get_code
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera flagę wskazującą, czy sekcja zawiera kod wykonywalny.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT get_code (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Zwraca `TRUE` Jeśli sekcja zawiera kod wykonywalny; w przeciwnym razie zwraca `FALSE`.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`. Zwraca `S_FALSE` Jeśli ta właściwość nie jest obsługiwana. W przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)



