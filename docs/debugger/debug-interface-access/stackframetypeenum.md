---
title: Stackframetypeenum — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- StackFrameTypeEnum enumeration
ms.assetid: 61e40163-eee0-4c1f-af47-cef3771bdc41
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: fcf5e120e769b69c064306432c3026194eb0d851
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49853940"
---
# <a name="stackframetypeenum"></a>StackFrameTypeEnum
Określa typ ramki stosu.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
enum StackFrameTypeEnum {  
   FrameTypeFPO,  
   FrameTypeTrap,  
   FrameTypeTSS,  
   FrameTypeStandard,  
   FrameTypeFrameData,  
   FrameTypeUnknown = -1  
};  
```  
  
## <a name="elements"></a>Elementy  
 `FrameTypeFPO`  
 Wskaźnik ramki pominięta; FPO informacji.  
  
 `FrameTypeTrap`  
 Ramka pułapki jądra.  
  
 `FrameTypeTSS`  
 Ramka pułapki jądra.  
  
 `FrameTypeStandard`  
 Standardowa EBP ramki stosu.  
  
 `FrameTypeFrameData`  
 Wskaźnik ramki pominięta; Ramka danych informacji.  
  
 `FrameTypeUnknown`  
 Ramki, który nie ma żadnych informacji o debugowaniu.  
  
## <a name="remarks"></a>Uwagi  
 Wartości w tym wyliczeniu są zwracane przez wywołanie [idiastackframe::get_type —](../../debugger/debug-interface-access/idiastackframe-get-type.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: cvconst.h  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia i struktury](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaStackFrame::get_type](../../debugger/debug-interface-access/idiastackframe-get-type.md)