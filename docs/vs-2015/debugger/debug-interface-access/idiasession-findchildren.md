---
title: Idiasession::findchildren — | Dokumentacja firmy Microsoft
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
helpviewer_keywords:
- IDiaSession::findChildren method
ms.assetid: 5d19046f-f668-4aa9-8788-95cda9a98997
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8ed41228f203997505161dcaeba9776afd73419e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49265124"
---
# <a name="idiasessionfindchildren"></a>IDiaSession::findChildren
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera wszystkie obiekty podrzędne identyfikatora określonego elementu nadrzędnego, które jest zgodny z typem nazwy i symboli.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
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
  
```cpp#  
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



