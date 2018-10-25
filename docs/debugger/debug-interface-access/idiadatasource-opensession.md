---
title: Idiadatasource::opensession — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::openSession method
ms.assetid: a3319ed0-3979-483b-9852-c0af96852c48
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8266102e8bc2c347ed8a554a3c64d9504f1e863b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49933511"
---
# <a name="idiadatasourceopensession"></a>IDiaDataSource::openSession
Zostanie otwarta sesja zapytań symboli.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT openSession (   
   IDiaSession** ppSession  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 ppSession  
 [out] Zwraca [idiasession —](../../debugger/debug-interface-access/idiasession.md) obiekt reprezentujący Otwórz sesję.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. W poniższej tabeli przedstawiono możliwe wartości zwracane dla tej metody.  
  
|Wartość|Opis|  
|-----------|-----------------|  
|WARTOŚĆ E_UNEXPECTED|[Idiadatasource —](../../debugger/debug-interface-access/idiadatasource.md) obiektu nie wcześniej została zainicjowana przy użyciu źródła symboli.|  
|E_INVALIDARG|Nieprawidłowy `ppSession` parametru.|  
|E_OUTOFMEMORY|Za mało pamięci, aby otworzyć sesji.|  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda otwiera [idiasession —](../../debugger/debug-interface-access/idiasession.md) obiekt dla źródła danych.  
  
 `IDiaSession` obiekty zaimplementować zapytania do źródła danych. Sesja zarządza jednej przestrzeni adresowej dla każdego zestawu symboli debugowania. Jeśli plik .exe lub .dll, opisanego przez symbole źródło danych jest aktywny adres wielu zakresów (na przykład, ponieważ wiele procesów jest załadowany), a następnie używać jednej sesji dla każdego zakresu adresów.  
  
## <a name="example"></a>Przykład  
  
```C++  
IDiaSession* pSession;  
HRESULT hr = pSource->openSession( &pSession );  
if (FAILED(hr))  
{  
   // report error  
}  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Idiadatasource —](../../debugger/debug-interface-access/idiadatasource.md)   
 [Omówienie](../../debugger/debug-interface-access/overview-debug-interface-access-sdk.md)   
 [Idiasession —](../../debugger/debug-interface-access/idiasession.md)   
 [Używanie zapytań dotyczących pliku .Pdb](../../debugger/debug-interface-access/querying-the-dot-pdb-file.md)