---
title: IDiaSymbol::get_frontEndBuild | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSymbol::get_frontEndBuild method
ms.assetid: f7dab1c6-112b-4966-baa5-afc976949c76
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 51659c76daac9195223bb4095e48aee56de22cb3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasymbolgetfrontendbuild"></a>IDiaSymbol::get_frontEndBuild
Pobiera numer kompilacji frontonu.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_frontEndBuild (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Zwraca numer kompilacji frontonu. Zobacz uwagi.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` lub kod błędu.  
  
> [!NOTE]
>  Zwracana wartość `S_FALSE` oznacza, że właściwość nie jest dostępna symbolu.  
  
## <a name="remarks"></a>Uwagi  
 Kompilator zazwyczaj składa się z dwóch podstawowe elementy: frontonu (analizator), która obsługuje analizowania kodu źródłowego w postaci pośredniej, oraz zaplecze (generator kodu), konwertująca pośredniego formularza do zestawu. Nie jest rzadko frontonem ma inną wersję niż wewnętrznej.  
  
 Frontonu lub zaplecza numer wersji składa się z trzech części: \<głównych >.\< drobne >. \<kompilacji >, gdzie \<głównych > numer wersji głównej \<pomocnicza > jest numerem wersji pomocniczej i \<kompilacji > jest numer kompilacji. Na przykład 13.10.3077.  
  
## <a name="requirements"></a>Wymagania  
  
|Wymaganie|Opis|  
|-----------------|-----------------|  
|Nagłówek:|dia2.h|  
|Wersja:|V7.0 DIA SDK|  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)