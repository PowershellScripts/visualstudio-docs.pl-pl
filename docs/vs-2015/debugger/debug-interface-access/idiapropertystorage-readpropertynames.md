---
title: IDiaPropertyStorage::ReadPropertyNames | Dokumentacja firmy Microsoft
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
- IDiaPropertyStorage::ReadPropertyNames
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4dd1027d5921af482a71c7c45e5b6c90599df512
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49232833"
---
# <a name="idiapropertystoragereadpropertynames"></a>IDiaPropertyStorage::ReadPropertyNames
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera odpowiadający nazwy ciągu dla danej właściwości identyfikatorów.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT ReadPropertyNames (  
   ULONG         cpropid,  
   PROPID const* rgpropid,  
   BSTR*         rglpwstrName  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `cpropid`  
 [in] Liczba identyfikatorów właściwości w `rgpropid`.  
  
 `rgpropid`  
 [in] Tablica identyfikatory właściwości, dla którego można pobrać nazwy (`PROPID` jest zdefiniowany w WTypes.h jako `ULONG`).  
  
 `rglpwstrName`  
 [out w] Tablica nazwy właściwości dla identyfikatorów określonej właściwości. Tablica musi być wstępnie przydzielić do przechowywania żądana liczba nazw właściwości i musi być w stanie co najmniej `cpropid``BSTR` ciągów.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Nazwy właściwości zwracanego należy oddzielić (przez wywołanie metody `SysFreeString` funkcji) kiedy są już potrzebne.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)



