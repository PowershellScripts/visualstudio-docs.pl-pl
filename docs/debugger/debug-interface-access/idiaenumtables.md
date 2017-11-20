---
title: "Idiaenumtables — | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumTables interface
ms.assetid: 016190c5-09e4-48f2-bf60-9b02603a03e0
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 913fdcefc4e90ea09030e416cb6a300e50855478
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiaenumtables"></a>IDiaEnumTables
Wylicza w różnych tabelach zawartych w źródle danych.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDiaEnumTables : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Metody w kolejności Vtable  
 W poniższej tabeli przedstawiono metody `IDiaEnumTables`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[IDiaEnumTables::get__NewEnum](../../debugger/debug-interface-access/idiaenumtables-get-newenum.md)|Pobiera [interfejsu interfejsu IEnumVARIANT](http://msdn.microsoft.com/en-us/139e3c93-faef-4003-9079-e0e94494db3e) wersji ten moduł wyliczający.|  
|[IDiaEnumTables::get_Count](../../debugger/debug-interface-access/idiaenumtables-get-count.md)|Pobiera liczbę tabel.|  
|[IDiaEnumTables::Item](../../debugger/debug-interface-access/idiaenumtables-item.md)|Pobiera tabeli za pomocą indeksu lub nazwę.|  
|[IDiaEnumTables::Next](../../debugger/debug-interface-access/idiaenumtables-next.md)|Pobiera określoną liczbę tabel w kolejności wyliczenia.|  
|[IDiaEnumTables::Skip](../../debugger/debug-interface-access/idiaenumtables-skip.md)|Pomija określoną liczbę tabel w kolejności wyliczenia.|  
|[IDiaEnumTables::Reset](../../debugger/debug-interface-access/idiaenumtables-reset.md)|Resetuje sekwencję wyliczenia na początku.|  
|[IDiaEnumTables::Clone](../../debugger/debug-interface-access/idiaenumtables-clone.md)|Tworzy moduł wyliczający, który zawiera takim samym stanie wyliczenie jako bieżący modułu wyliczającego.|  
  
## <a name="remarks"></a>Uwagi  
  
## <a name="notes-for-callers"></a>Uwagi dotyczące wywoływania  
 Uzyskanie przez wywołanie metody tego interfejsu [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession-getenumtables.md) metody.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie pokazano, jak uzyskać `IDiaEnumTables` interfejsu z sesji. Aby uzyskać bardziej szczegółowy przykład przy użyciu tabel, zobacz [idiatable —](../../debugger/debug-interface-access/idiatable.md) interfejsu.  
  
```C++  
void ShowTableNames(IDiaSession *pSession)  
{  
    CComPtr<IDiaEnumTables> pTables;  
    if ( FAILED( psession->getEnumTables( &pTables ) ) )  
    {  
        Fatal( "getEnumTables" );  
    }  
    // Do something with table  
}  
```  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: Dia2.h  
  
 Biblioteki: diaguids.lib  
  
 Biblioteki DLL: msdia80.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejsy (zestaw SDK dostępu do interfejsu debugowania)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession-getenumtables.md)