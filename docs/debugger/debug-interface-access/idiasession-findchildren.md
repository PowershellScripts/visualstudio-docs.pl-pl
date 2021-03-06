---
title: Idiasession::findchildren — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findChildren method
ms.assetid: 5d19046f-f668-4aa9-8788-95cda9a98997
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 16033fc289e5a1fe2a8331e927bba51ce1671fd2
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49896175"
---
# <a name="idiasessionfindchildren"></a>IDiaSession::findChildren
Pobiera wszystkie obiekty podrzędne identyfikatora określonego elementu nadrzędnego, które jest zgodny z typem nazwy i symboli.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT findChildren (   
   IDiaSymbol*       parent,  
   SymTagEnum        symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `parent`  
 [in] [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md) obiekt reprezentujący element nadrzędny. Jeśli ten symbol nadrzędnego jest funkcja, modułu lub blok, a następnie jego leksykalne elementy podporządkowane są zwracane w `ppResult`. Jeśli nadrzędny symbol jest typem, jego elementów podrzędnych klasy są zwracane. Jeśli ten parametr jest `NULL`, następnie `symtag` musi być równa `SymTagExe` lub `SymTagNull`, która zwraca zakresu globalnego (plik .exe).  
  
 `symtag`  
 [in] Określa symbol znacznika elementów podrzędnych, które mają zostać pobrane. Wartości są pobierane z [symtagenum — wyliczenie](../../debugger/debug-interface-access/symtagenum.md) wyliczenia. Ustaw `SymTagNull` można pobrać wszystkie elementy podrzędne.  
  
 `name`  
 [in] Określa nazwę elementy podrzędne, które mają zostać pobrane. Ustaw `NULL` dla wszystkich elementów podrzędnych do pobrania.  
  
 `compareFlags`  
 [in] Określa opcje porównywania stosowany do pasujących nazwy. Wartości z kolekcji [namesearchoptions — wyliczenie](../../debugger/debug-interface-access/namesearchoptions.md) wyliczenia można samodzielnie lub w połączeniu.  
  
 `ppResult`  
 [out] Zwraca [idiaenumsymbols —](../../debugger/debug-interface-access/idiaenumsymbols.md) pobrać obiekt, który zawiera listę symbolami podrzędnymi.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak znaleźć zmiennych lokalnych funkcji `pFunc` wpisywanych dopasowanie `szVarName`.  
  
```C++  
IDiaEnumSymbols* pEnum;  
pSession->findChildren( pFunc, SymTagData, szVarName, nsCaseSensitive, &pEnum );  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Omówienie](../../debugger/debug-interface-access/overview-debug-interface-access-sdk.md)   
 [Idiaenumsymbols —](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)   
 [Namesearchoptions — wyliczenie](../../debugger/debug-interface-access/namesearchoptions.md)   
 [SymTagEnum, wyliczenie](../../debugger/debug-interface-access/symtagenum.md)