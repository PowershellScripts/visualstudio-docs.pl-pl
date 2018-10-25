---
title: IDiaSession::findAcceleratorInlineesByLinenum | Dokumentacja firmy Microsoft
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
ms.assetid: 386c87aa-f7b2-4d38-9dd6-fffba9ff01f0
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7591c0dc3654387c848fe447fcb17f72143c78a0
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49900205"
---
# <a name="idiasessionfindacceleratorinlineesbylinenum"></a>IDiaSession::findAcceleratorInlineesByLinenum
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Zwraca wyliczenie symboli dla ramek wbudowanych, które odnoszą się do określonej lokalizacji źródłowej.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT findAcceleratorInlineeLinesByName (   
   IDiaSymbol*           parent,  
   IDiaSourceFile*       file,  
   DWORD                 linenum,  
   DWORD                 colnum,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `parent`  
 [in] `IDiaSymbol` Odnosi się do funkcji klasy zastępczej akceleratora, która ma być przeszukiwany.  
  
 `file`  
 [in] `IDiaSourceFile` Lokalizacji źródła.  
  
 `linenum`  
 [in] Numer wiersza lokalizacji źródła.  
  
 `colnum`  
 [in] Numer kolumny lokalizacji źródła.  
  
 `ppResult`  
 [out] Wskaźnik do `IDiaEnumLineNumbers` wskaźnik interfejsu, który jest inicjowany z wynikiem.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)   
 [Idiaenumlinenumbers —](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



