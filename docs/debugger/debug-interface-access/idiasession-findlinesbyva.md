---
title: IDiaSession::findLinesByVA | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSession::findLinesByVA method
ms.assetid: f647eee9-a73c-483b-9fe9-21f42e560a7b
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ba8c06066c78505d915834f2ffcc1d8c634a1c73
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasessionfindlinesbyva"></a>IDiaSession::findLinesByVA
Pobiera informacje o numer wiersza dla wierszy znajdujących się w zakresie określonym wirtualnego adresu (VA).  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT findLinesByVA (   
   ULONGLONG             va,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `va`  
 [in] Określa adres jako VA.  
  
 `length`  
 [in] Określa liczbę bajtów zakres adresów, aby pokrywał się z tym zapytaniem.  
  
 `ppResult`  
 [out] Zwraca [idiaenumlinenumbers —](../../debugger/debug-interface-access/idiaenumlinenumbers.md) obiekt, który zawiera listę wszystkich linii numery ochrona ta określony zakres adresów.  
  
## <a name="example"></a>Przykład  
 Ten przykład przedstawia funkcję, która uzyskuje wszystkie numery wierszy zawartych w funkcji za pomocą funkcji wirtualnego adresu i długości.  
  
```C++  
IDiaEnumLineNumbers *GetLineNumbersByVA(IDiaSymbol *pFunc, IDiaSession *pSession)  
{  
    IDiaEnumLineNumbers* pEnum = NULL;  
    ULONGLONG            va;  
    ULONGLONG            length;  
  
    if (pFunc->get_virtualAddress ( &va ) == S_OK)  
    {  
        pFunc->get_length( &length );  
        pSession->findLinesByVA( va, static_cast<DWORD>( length ), &pEnum );  
    }  
    return(pEnum);  
}  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Idiaenumlinenumbers —](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)