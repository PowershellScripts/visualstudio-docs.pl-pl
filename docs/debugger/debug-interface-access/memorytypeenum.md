---
title: "Memorytypeenum — | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: MemoryTypeEnum enumeration
ms.assetid: 8778c047-edeb-4495-8f9f-3f8bbb297099
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: db6a66f8d496c73d05e05fd2f5398998c0a72484
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="memorytypeenum"></a>MemoryTypeEnum
Określa typ pamięci, aby uzyskać dostęp.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
enum MemoryTypeEnum {  
   MemTypeCode,  
   MemTypeData,  
   MemTypeStack,  
   MemTypeAny = -1  
};  
```  
  
#### <a name="parameters"></a>Parametry  
 `MemTypeCode`  
 Uzyskuje dostęp do kodu tylko pamięci.  
  
 `MemTypeData`  
 Uzyskuje dostęp do danych lub stosu pamięci.  
  
 `MemTypeStack`  
 Dostęp tylko stosu pamięci.  
  
 `MemTypeAny`  
 Uzyskuje dostęp do dowolnego rodzaju pamięci.  
  
## <a name="remarks"></a>Uwagi  
 Wartości w tym wyliczeniu są przekazywane do [IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md) metodę, aby ograniczyć dostęp do różnych rodzajów pamięci.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: cvconst.h  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia i struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md)