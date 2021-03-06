---
title: Idiaenumframedata — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumFrameData interface
ms.assetid: 2ca7fd5a-b2fa-4b3a-9492-0263eafc435b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c39057a77da9b459852e0b591ea8d69186ee6f8d
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/18/2018
ms.locfileid: "31466930"
---
# <a name="idiaenumframedata"></a>IDiaEnumFrameData
Wylicza różne elementy danych ramki zawarte w źródle danych.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDiaEnumFrameData : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Metody w kolejności Vtable  
 W poniższej tabeli przedstawiono metody `IDiaEnumFrameData`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[IDiaEnumFrameData::get__NewEnum](../../debugger/debug-interface-access/idiaenumframedata-get-newenum.md)|Pobiera `IEnumVARIANT Interface` wersji ten moduł wyliczający.|  
|[IDiaEnumFrameData::get_Count](../../debugger/debug-interface-access/idiaenumframedata-get-count.md)|Pobiera liczbę elementów danych ramki.|  
|[IDiaEnumFrameData::Item](../../debugger/debug-interface-access/idiaenumframedata-item.md)|Pobiera element danych ramki za pomocą indeksu.|  
|[IDiaEnumFrameData::Next](../../debugger/debug-interface-access/idiaenumframedata-next.md)|Pobiera określoną liczbę elementów danych ramki w kolejności wyliczenia.|  
|[IDiaEnumFrameData::Skip](../../debugger/debug-interface-access/idiaenumframedata-skip.md)|Pomija określoną liczbę elementów danych ramki w kolejności wyliczenia.|  
|[IDiaEnumFrameData::Reset](../../debugger/debug-interface-access/idiaenumframedata-reset.md)|Resetuje sekwencję wyliczenia na początku.|  
|[IDiaEnumFrameData::Clone](../../debugger/debug-interface-access/idiaenumframedata-clone.md)|Tworzy moduł wyliczający, który zawiera takim samym stanie wyliczenie jako bieżący modułu wyliczającego.|  
|[IDiaEnumFrameData::frameByRVA](../../debugger/debug-interface-access/idiaenumframedata-framebyrva.md)|Zwraca ramki przez wirtualny adres względny (RVA).|  
|[IDiaEnumFrameData::frameByVA](../../debugger/debug-interface-access/idiaenumframedata-framebyva.md)|Przywraca ramkę wirtualnego adresu (VA).|  
  
## <a name="remarks"></a>Uwagi  
  
## <a name="notes-for-callers"></a>Uwagi dotyczące wywoływania  
 Uzyskaj ten interfejs z [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession-getenumtables.md) metody. Zapoznaj się z przykładem, aby uzyskać szczegółowe informacje.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie pokazano, jak uzyskać ( `GetEnumFrameData` funkcji) i użyj ( `ShowFrameData` funkcji) `IDiaEnumFrameData` interfejsu. Zobacz [idiaframedata —](../../debugger/debug-interface-access/idiaframedata.md) interfejsu przykład `PrintFrameData` funkcji.  
  
```C++  
  
      IDiaEnumFrameData* GetEnumFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pUnknown    = NULL;  
    REFIID             iid         = __uuidof(IDiaEnumFrameData);  
    IDiaEnumTables*    pEnumTables = NULL;  
    IDiaTable*         pTable      = NULL;  
    ULONG              celt        = 0;  
  
    if (pSession->getEnumTables(&pEnumTables) != S_OK)  
    {  
        wprintf(L"ERROR - GetTable() getEnumTables\n");  
        return NULL;  
    }  
    while (pEnumTables->Next(1, &pTable, &celt) == S_OK && celt == 1)  
    {  
        // There is only one table that matches the given iid  
        HRESULT hr = pTable->QueryInterface(iid, (void**)&pUnknown);  
        pTable->Release();  
        if (hr == S_OK)  
        {  
            break;  
        }  
    }  
    pEnumTables->Release();  
    return pUnknown;  
}  
  
void ShowFrameData(IDiaSession *pSession)  
{  
    IDiaEnumFrameData* pEnumFrameData = GetEnumFrameData(pSession);;  
  
    if (pEnumFrameData != NULL)  
    {  
        IDiaFrameData* pFrameData;  
        ULONG celt = 0;  
  
        while(pEnumFrameData->Next(1, &pFrameData, &celt) == S_OK &&  
              celt == 1)  
        {  
            PrintFrameData(pFrameData);  
            pFrameData->Release();  
        }  
        pEnumFrameData->Release();   
    }  
}  
```  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** Dia2.h  
  
 **Biblioteka:** diaguids.lib  
  
 **Biblioteki DLL:** msdia80.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejsy (zestaw SDK dostępu do interfejsu debugowania)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession-getenumtables.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)