---
title: IDiaSession::getEnumTables | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSession::getEnumTables method
ms.assetid: 66e0fba2-ca63-4e24-a46a-c99c7fb61dd1
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 59061e02dcfefb1e841ea5b6a8947bb1a8af4bfa
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasessiongetenumtables"></a>IDiaSession::getEnumTables
Pobiera moduł wyliczający dla wszystkich tabel znajdujących się w magazynie symboli.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT getEnumTables (   
   IDiaEnumTables** ppEnumTables  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnumTables`  
 [out] Zwraca [idiaenumtables —](../../debugger/debug-interface-access/idiaenumtables.md) obiektu. Ten interfejs umożliwia wyliczyć tabel w magazynie symboli.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie przedstawiono ogólne funkcję, która używa `getEnumTables` metody uzyskanie obiektu określonego modułu wyliczającego. Jeśli zostanie znaleziony moduł wyliczający, funkcja zwraca wskaźnik, które mogą być rzutowane na żądany interfejs; w przeciwnym razie funkcja zwraca `NULL`.  
  
```C++  
IUnknown *GetTable(IDiaSession *pSession, REFIID iid)  
{  
    IUnknown *pUnknown = NULL;  
    if (pSession != NULL)  
    {  
        CComPtr<IDiaEnumTables> pEnumTables;  
        if (pSession->getEnumTables(&pEnumTables) == S_OK)  
        {  
             CComPtr<IDiaTable> pTable;  
             DWORD celt = 0;  
             while(pEnumTables->Next(1,&pTable,&celt) == S_OK &&  
                   celt == 1)  
             {  
                  if (pTable->QueryInterface(iid, (void **)pUnknown) == S_OK)  
                  {  
                       break;  
                  }  
                  pTable = NULL;  
             }  
        }  
    }  
    return(pUnknown);  
}  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumtables —](../../debugger/debug-interface-access/idiaenumtables.md)   
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)