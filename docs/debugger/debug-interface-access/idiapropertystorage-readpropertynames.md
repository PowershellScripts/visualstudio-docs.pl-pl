---
title: IDiaPropertyStorage::ReadPropertyNames | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadPropertyNames
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4d51eaed785932703a5eb97714be8dc7b407fc81
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49891820"
---
# <a name="idiapropertystoragereadpropertynames"></a>IDiaPropertyStorage::ReadPropertyNames
Pobiera odpowiadający nazwy ciągu dla danej właściwości identyfikatorów.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
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