---
title: IDiaSession::findInlineeLinesByRVA | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 7a74d5ee-0dbf-47c0-92b4-47ec03b13ce9
caps.latest.revision: "3"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5210616573d2d1e0248c189095c8f10e192eab80
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasessionfindinlineelinesbyrva"></a>IDiaSession::findInlineeLinesByRVA
Pobiera wyliczenie umożliwia klientowi Iterowanie za pomocą informacji o numerze linii wszystkie funkcje, które są wbudowane, bezpośrednio lub pośrednio, za pomocą symbolu określonego elementu nadrzędnego, który są zawarte w określonej wirtualnej adres względny (RVA).  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT findInlineeLinesByRVA (   
   IDiaSymbol*           parent,  
   DWORD                 rva,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `parent`  
 [in] `IDiaSymbol` Obiekt reprezentujący element nadrzędny.  
  
 `rva`  
 [in] Określa adres co adres RVA.  
  
 `length`  
 [in] Określa zakres adresów w liczba bajtów, aby pokrywał się z tym zapytaniem.  
  
 `ppResult`  
 [out] Przechowuje `IDiaEnumLineNumbers` obiekt, który zawiera listę numerów wierszy, które są pobierane.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)   
 [Symtagenum — wyliczenie](../../debugger/debug-interface-access/symtagenum.md)   
 [Idiaenumlinenumbers —](../../debugger/debug-interface-access/idiaenumlinenumbers.md)