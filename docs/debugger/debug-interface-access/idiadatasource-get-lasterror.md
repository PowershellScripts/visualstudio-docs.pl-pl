---
title: Idiadatasource::get_lasterror — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::get_lastError method
ms.assetid: cf08850b-8b75-4e8c-90bd-bd0214756f99
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e197262b84fcf964afb74f85e86ff384daa26c9e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49819840"
---
# <a name="idiadatasourcegetlasterror"></a>IDiaDataSource::get_lastError
Pobiera nazwę pliku dla ostatniego błędu ładowania.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_lastError (  
   BSTR* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pRetVal  
 [out] Zwraca ciąg, który zawiera nazwę pliku .pdb, które są skojarzone z ostatniego błędu ładowania.  
  
## <a name="return-value"></a>Wartość zwracana  
 Zwraca kod ostatniego błędu spowodowanych operacji ładowania. Zwraca `E_INVALIDARG` Jeśli `pRetVal` parametr `NULL`.  
  
## <a name="example"></a>Przykład  
  
```C++  
BSTR    fileName;  
HRESULT errorCode = pSource->get_lastError( &fileName );  
```  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaDataSource](../../debugger/debug-interface-access/idiadatasource.md)