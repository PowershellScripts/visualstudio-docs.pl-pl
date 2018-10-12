---
title: IDiaSymbol::get_subTypeId | Dokumentacja firmy Microsoft
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
ms.assetid: 0f899920-4fc5-4de8-84a3-cd98c57bf124
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: af506a2598d5ba4d8c8722acc585fc717b8d1cdd
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49217101"
---
# <a name="idiasymbolgetsubtypeid"></a>IDiaSymbol::get_subTypeId
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera identyfikator podrzędnego typu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT get_subTypeId(   
   DWORD* pRetVal);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Wskaźnik do `DWORD` zawierający identyfikator podrzędnego typu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` albo kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



