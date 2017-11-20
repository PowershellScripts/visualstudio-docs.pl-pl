---
title: "Idiapropertystorage — | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaPropertyStorage interface
ms.assetid: d3197a38-5973-4e56-873e-4f1b84c3f674
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1a135bb036a327433ba3edb3e6e320a2d81a279e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiapropertystorage"></a>IDiaPropertyStorage
Umożliwia odczytanie trwałej właściwości zestaw właściwości DIA.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDiaPropertyStorage : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Metody w kolejności Vtable  
 W poniższej tabeli przedstawiono metody `IDiaPropertyStorage`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[IDiaPropertyStorage::Enum](../../debugger/debug-interface-access/idiapropertystorage-enum.md)|Pobiera wskaźnik do modułu wyliczającego dla właściwości w tym zestawie.|  
|[IDiaPropertyStorage::ReadBOOL](../../debugger/debug-interface-access/idiapropertystorage-readbool.md)|Odczytuje `BOOL` wartości w zestawie właściwości.|  
|[IDiaPropertyStorage::ReadBSTR](../../debugger/debug-interface-access/idiapropertystorage-readbstr.md)|Odczytuje `BSTR` wartości w zestawie właściwości.|  
|[IDiaPropertyStorage::ReadDWORD](../../debugger/debug-interface-access/idiapropertystorage-readdword.md)|Odczytuje `DWORD` wartości w zestawie właściwości.|  
|[IDiaPropertyStorage::ReadLONG](../../debugger/debug-interface-access/idiapropertystorage-readlong.md)|Odczytuje `LONG` wartości w zestawie właściwości.|  
|[IDiaPropertyStorage::ReadMultiple](../../debugger/debug-interface-access/idiapropertystorage-readmultiple.md)|Odczytuje wartości właściwości w zestawie właściwości.|  
|[IDiaPropertyStorage::ReadPropertyNames](../../debugger/debug-interface-access/idiapropertystorage-readpropertynames.md)|Pobiera odpowiednie nazwy ciągów dla danego identyfikatory właściwości.|  
|[IDiaPropertyStorage::ReadULONGLONG](../../debugger/debug-interface-access/idiapropertystorage-readulonglong.md)|Odczytuje `ULONGLONG` wartości w zestawie właściwości.|  
  
## <a name="remarks"></a>Uwagi  
 Każdej właściwości w zestawie właściwości jest identyfikowany przez identyfikator właściwości (ID), 4 bajtowych `ULONG` unikatowe dla tego zestawu wartości. Właściwości, za pośrednictwem `IDiaPropertyStorage` interfejsu odpowiada właściwości dostępne w interfejsie nadrzędnej. Na przykład właściwości [idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) interfejsu można uzyskać, sprawdzając nazwę za pośrednictwem `IDiaPropertyStorage` interfejsu (należy jednak pamiętać, że nawet jeśli właściwość może być dostępny, nie oznacza to, jest nieprawidłowa dla właściwości określonego `IDiaSymbol` obiektu).  
  
## <a name="notes-for-callers"></a>Uwagi dotyczące wywoływania  
 Uzyskanie przez wywołanie metody tego interfejsu `QueryInterface` metody na inny interfejs. Następujące interfejsy mogą być przeszukiwane dla `IDiaPropertyStorage` interfejsu:  
  
-   [Idiasectioncontrib —](../../debugger/debug-interface-access/idiasectioncontrib.md)  
  
-   [Idiasegment —](../../debugger/debug-interface-access/idiasegment.md)  
  
-   [Idiainjectedsource —](../../debugger/debug-interface-access/idiainjectedsource.md)  
  
-   [Idiaframedata —](../../debugger/debug-interface-access/idiaframedata.md)  
  
-   [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)  
  
-   [Idiasourcefile —](../../debugger/debug-interface-access/idiasourcefile.md)  
  
-   [Idialinenumber —](../../debugger/debug-interface-access/idialinenumber.md)  
  
## <a name="example"></a>Przykład  
 Ten przykład przedstawia funkcję, która wyświetla wszystkie właściwości udostępniane przez `IDiaPropertyStorage` obiektu. Zobacz [idiaenuminjectedsources —](../../debugger/debug-interface-access/idiaenuminjectedsources.md) interfejsu, na przykład przedstawia sposób `IDiaPropertyStorage` interfejsu są uzyskiwane z [idiainjectedsource —](../../debugger/debug-interface-access/idiainjectedsource.md) interfejsu.  
  
```C++  
void PrintPropertyStorage(IDiaPropertyStorage* pPropertyStorage)  
{  
    IEnumSTATPROPSTG* pEnumProps;  
    STATPROPSTG       prop;  
    DWORD             celt = 1;  
  
    if (pPropertyStorage->Enum(&pEnumProps) == S_OK)  
    {  
        while (pEnumProps->Next(celt, &prop, &celt) == S_OK)  
        {  
            PROPSPEC pspec = { PRSPEC_PROPID, prop.propid };  
            PROPVARIANT vt = { VT_EMPTY };  
  
            if (pPropertyStorage->ReadMultiple( 1, &pspec, &vt) == S_OK)  
            {  
                switch( vt.vt ){  
                    case VT_BOOL:  
                        wprintf( L"%32s:\t %s\n", prop.lpwstrName, vt.bVal ? L"true" : L"false" );  
                        break;  
                    case VT_I2:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.iVal );  
                        break;  
                    case VT_UI2:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.uiVal );  
                        break;  
                    case VT_I4:  
                        wprintf( L"%32s:\t %d\n", prop.lpwstrName, vt.intVal );  
                        break;  
                    case VT_UI4:  
                        wprintf( L"%32s:\t 0x%0x\n", prop.lpwstrName, vt.uintVal );  
                        break;  
                    case VT_UI8:  
                        wprintf( L"%32s:\t 0x%x\n", prop.lpwstrName, vt.uhVal.QuadPart );  
                        break;  
                    case VT_BSTR:  
                        wprintf( L"%32s:\t %s\n", prop.lpwstrName, vt.bstrVal );  
                        break;  
                    case VT_UNKNOWN:  
                        wprintf( L"%32s:\t %p\n", prop.lpwstrName, vt.punkVal );  
                        break;  
                    case VT_SAFEARRAY:  
                        break;  
                    default:  
                       break;  
                }  
                VariantClear((VARIANTARG*) &vt);  
            }  
        }  
        pEnumProps->Release();  
    }  
}  
```  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: Dia2.h  
  
 Biblioteki: diaguids.lib  
  
 Biblioteki DLL: msdia80.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejsy (zestaw SDK dostępu do interfejsu debugowania)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaSession::getEnumTables](../../debugger/debug-interface-access/idiasession-getenumtables.md)   
 [Idiasectioncontrib —](../../debugger/debug-interface-access/idiasectioncontrib.md)   
 [Idiasegment —](../../debugger/debug-interface-access/idiasegment.md)   
 [Idiainjectedsource —](../../debugger/debug-interface-access/idiainjectedsource.md)   
 [Idiaframedata —](../../debugger/debug-interface-access/idiaframedata.md)   
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasourcefile —](../../debugger/debug-interface-access/idiasourcefile.md)   
 [Idialinenumber —](../../debugger/debug-interface-access/idialinenumber.md)   
 [Idiaenuminjectedsources —](../../debugger/debug-interface-access/idiaenuminjectedsources.md)