---
title: IDiaSourceFile::get_checksumType | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaSourceFile::get_checksumType method
ms.assetid: 4c363e61-a6a9-409a-9cc0-d06eb2bee645
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8fafd9e813c22b899603a2e62c5a2c90ece1a709
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idiasourcefilegetchecksumtype"></a>IDiaSourceFile::get_checksumType
Pobiera typ sumy kontrolnej.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT get_checksumType (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Zwraca typ sumy kontrolnej.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Typ Suma kontrolna jest wartość, która może być zmapowana do algorytmu sumy kontrolnej. Na przykład standardowy format pliku PDB zwykle może mieć jedną z następujących wartości:  
  
|Typ sumy kontrolnej|Etykieta CryptoAPI|Opis|  
|-------------------|---------------------|-----------------|  
|0|\<Brak >|Nie istnieje sumy kontrolnej.|  
|1|`CALG_MD5`|Suma kontrolna wygenerowanych przy użyciu algorytmu wyznaczania wartości skrótu MD5.|  
|2|`CALG_SHA1`|Suma kontrolna wygenerowanych przy użyciu algorytmu wyznaczania wartości skrótu SHA1.|  
  
 `CryptoAPI` Etykiety są z `ALG_ID` wyliczenia. Aby uzyskać więcej informacji dotyczących tworzenia skrótów algorytmów, zapoznaj się `CryptoAPI` części programu Microsoft [!INCLUDE[winsdkshort](../../debugger/debug-interface-access/includes/winsdkshort_md.md)].  
  
 Aby uzyskać bajtów rzeczywista suma kontrolna dla pliku źródłowego, należy wywołać [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasourcefile —](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)