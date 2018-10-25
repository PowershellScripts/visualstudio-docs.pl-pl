---
title: Idiastackwalkframe::searchforreturnaddressstart — | Dokumentacja firmy Microsoft
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
- IDiaStackWalkFrame::searchForReturnAddressStart method
ms.assetid: 47660b9b-6e4f-4dfa-88ab-63dce28f7412
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d7c0079066266059163dd001de9be6b782319a24
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49849830"
---
# <a name="idiastackwalkframesearchforreturnaddressstart"></a>IDiaStackWalkFrame::searchForReturnAddressStart
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Wyszukuje ramki określonego stosu, dla adres zwrotny po lub w pobliżu podanym adresem.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT searchForReturnAddressStart (   
   IDiaFrameData* frame,  
   ULONGLONG      startAddress,  
   ULONGLONG*     returnAddress  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `frame`  
 [in] [Idiaframedata —](../../debugger/debug-interface-access/idiaframedata.md) obiekt, który reprezentuje bieżącą ramkę stosu.  
  
 `startAddress`  
 [in] Adres pamięci wirtualnej, z którego należy rozpocząć wyszukiwanie.  
  
 `returnAddress`  
 [out] Zwraca funkcję najbliższej zwrotny adres, który `startAddress`.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiastackwalkframe —](../../debugger/debug-interface-access/idiastackwalkframe.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)



