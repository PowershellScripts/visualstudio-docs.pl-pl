---
title: IDiaSymbol::findInlineeLinesByVA | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 61427d33-30d2-4ac9-9bd6-c58c6c705072
caps.latest.revision: "3"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 442dd8fce97c30cfce792f825d8212e6558bf4cb
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasymbolfindinlineelinesbyva"></a>IDiaSymbol::findInlineeLinesByVA
Pobiera wyliczenie umożliwia klientowi iterację informacja o numerach wierszy wszystkich funkcji, które są wbudowane, bezpośrednio lub pośrednio, w tym symbolu w ramach określonego wirtualnego adresu (VA).  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT findInlineeLinesByVA (   
   ULONGLONG             va,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `va`  
 [in] Określa adres jako VA.  
  
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