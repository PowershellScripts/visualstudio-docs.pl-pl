---
title: IDiaStackWalkHelper::get_registerValue | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaStackWalkHelper2::get_registerValue method
ms.assetid: 46ac5eee-73a3-44a1-8635-6c58ba193cb6
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 35d956b1d246d0a43ae058bb58635117c093602c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiastackwalkhelpergetregistervalue"></a>IDiaStackWalkHelper::get_registerValue
Pobiera wartość rejestru.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_registerValue (   
   DWORD      index,  
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `index`  
 [in] Wartość z zakresu od [cv_hreg_e — wyliczenie](../../debugger/debug-interface-access/cv-hreg-e.md) określenie, które Zarejestruj, aby pobrać wartości z wyliczenia.  
  
 `pRetVal`  
 [out] Zwraca bieżącą wartość rejestru.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Niezależnie od rozmiaru `pRetVal` parametru, co rejestru zwykle zawiera jedynie implementację powinny być przechowywane. Na przykład rejestr 8-bitową zawiera tylko najniższy 8-bitowej danej wartości. Ta wartość 8-bitowych jest rozwinięty, 64-bitowej, gdy zwracany przez tę metodę.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [Cv_hreg_e — wyliczenie](../../debugger/debug-interface-access/cv-hreg-e.md)