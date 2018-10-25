---
title: Idiasymbol::get_haslongjump — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hasLongJump method
ms.assetid: 14484cb1-43b0-47a1-a9a8-081b55566886
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7edf8e42e8c40ab9bbe5d032f026c23f8b7ff147
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49835829"
---
# <a name="idiasymbolgethaslongjump"></a>IDiaSymbol::get_hasLongJump
Pobiera flagę określającą, czy funkcja zawiera korzystanie z [longjmp](/cpp/c-runtime-library/reference/longjmp) polecenia (parowania z [setjmp](/cpp/c-runtime-library/reference/setjmp) polecenia tworzą one stylu C sposób obsługi wyjątków).  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_hasLongJump  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pFlag`  
 [out] Zwraca `TRUE` Jeśli funkcja zawiera `longjmp` polecenie; w przeciwnym razie zwraca `FALSE`.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` albo kod błędu.  
  
> [!NOTE]
>  Zwracana wartość wynosząca `S_FALSE` oznacza, że właściwość nie jest dostępna dla symbolu.  
  
## <a name="requirements"></a>Wymagania  
  
|Wymaganie|Opis|  
|-----------------|-----------------|  
|Nagłówek:|dia2.h|  
|Wersja:|DIA SDK w wersji 8.0|  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasymbol —](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasymbol::get_hassetjump —](../../debugger/debug-interface-access/idiasymbol-get-hassetjump.md)   
 [longjmp](/cpp/c-runtime-library/reference/longjmp)   
 [setjmp](/cpp/c-runtime-library/reference/setjmp)