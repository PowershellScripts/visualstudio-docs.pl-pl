---
title: Memorytypeenum — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MemoryTypeEnum enumeration
ms.assetid: 8778c047-edeb-4495-8f9f-3f8bbb297099
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4a8dcf657933cf62f3f2173bb89dadd1366b0cec
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49822946"
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
 Uzyskuje dostęp do tylko stosu pamięci.  
  
 `MemTypeAny`  
 Uzyskuje dostęp do dowolnego rodzaju pamięci.  
  
## <a name="remarks"></a>Uwagi  
 Wartości w tym wyliczeniu są przekazywane do [IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md) metodę, aby ograniczyć dostęp do różnych typów pamięci.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: cvconst.h  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia i struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md)